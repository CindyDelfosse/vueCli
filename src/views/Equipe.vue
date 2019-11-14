<template>
    <div class="contact container">
        <h1 class="title"> {{ titre | cap }} à {{ prix | prix('$') }} </h1>
        <hr>
        <div class="columns">
            <EquipePres v-for="membre in equipes" :key="membre.nom" :membre="membre"></EquipePres>
        </div>
    </div>
</template>

<script>
// @ is an alias to /src
import EquipePres from '@/components/EquipePres.vue'
import Capitalize from '@/filters/Capitalize'
import FormatEuro from '@/filters/FormatEuro'

export default {
  name: 'contact',
  data(){
    return {
        titre : "team",
        prix : 999.9888888,
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
  }, 
  filters: {
    cap: Capitalize, 
    prix: FormatEuro
  }
}
</script>
