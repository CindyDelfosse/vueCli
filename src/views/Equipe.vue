<template>
    <div class="contact container">
        <h1 class="title">Voici notre équipe</h1>
        <hr>
        <div class="columns">
            <EquipePres v-for="membre in equipes" :key="membre.nom" :membre="membre"></EquipePres>
        </div>
    </div>
</template>

<script>
// @ is an alias to /src
import EquipePres from '@/components/EquipePres.vue'

export default {
  name: 'contact',
  data(){
    return {
      equipes : [
          {
              'nom' : 'Delfosse',
              'prenom' : 'Cindy',
              'description' : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus nec iaculis mauris. ",
              'image' : 'https://picsum.photos/id/237/200/300',
              'tags' : ["#js", "#css", "#html"]
          },
          {
              'nom' : 'Smith',
              'prenom' : 'John',
              'description' : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus nec iaculis mauris. ",
              'image' : 'https://picsum.photos/id/238/200/300',
              'tags' : ["#js", "#css", "#html"]
          },
          {
              'nom' : 'Smith2',
              'prenom' : 'John2',
              'description' : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus nec iaculis mauris. ",
              'image' : 'https://picsum.photos/id/239/200/300',
              'tags' : ["#js", "#css", "#html"]
          },
      ]
    }
  },
  components: {
    EquipePres
  }
}
</script>
