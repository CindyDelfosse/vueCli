<template>
  <div class="equipe-pres">
        <div class="column" >    
            <div class="card">
                <div class="card-image">
                    <figure class="image is-4by3">
                    <img :src="membre.image" alt="Placeholder image">
                    </figure>
                </div>
                <div class="card-content">
                    <div class="media">
                    <div class="media-left">
                        <figure class="image is-48x48">
                        <img src="https://picsum.photos/200" alt="Placeholder image">
                        </figure>
                    </div>
                    <div class="media-content">
                        <p class="title is-4">{{membre.prenom}} {{membre.nom}}</p>
                        <p class="subtitle is-6">@{{membre.prenom}}{{membre.nom}}</p>
                    </div>
                    </div>

                    <div class="content">
                        {{ membre.description}}
                    <a href="#" v-for="(tag, index) in membre.tags" :key="index">{{tag}} </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'EquipePres',
  props: {
      membre: Object
  }
}
</script>

<style lang="scss">
    $colorButtonBack : #42b983;
    $colorButton : white;
    .button.my-button {
        background-color: $colorButtonBack;
        color: $colorButton;
    }
</style>
