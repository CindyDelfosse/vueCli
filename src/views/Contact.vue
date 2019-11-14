<template>
  <div class="contact">
    <h1 class="title">Contact</h1>
    <p>Nop pas possible pour le moment, nous n'avons pas de formulaire</p>
    <hr>
    <ContactForm msg="Maintenant oui"></ContactForm>
  </div>
</template>

<script>
// @ is an alias to /src
import ContactForm from '@/components/ContactForm.vue'

export default {
  name: 'contact',
  components: {
    ContactForm
  }
}
</script>
