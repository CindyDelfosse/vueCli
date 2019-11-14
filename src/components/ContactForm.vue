<template>
  <div class="contact-form">
    <p>Bientôt un formulaire ici dans le component</p>
    <h2 class="title"> {{ msg }} </h2>
    <div class="field">
        <label for="nom" class="label">Nom</label>
        <input type="text" class="input" placeholder="Nom Prénom">
    </div>
    <div class="field">
        <label for="email" class="label">Email</label>
        <div class="control has-icons-left has-icons-right">
            <input class="input" type="email" placeholder="hello@dom.com">
            <span class="icon is-small is-left">
            <i class="fas fa-envelope"></i>
            </span>
            <span class="icon is-small is-right">
            <i class="fas fa-exclamation-triangle"></i>
            </span>
        </div>
    </div>
    <div class="field">
        <label for="message" class="label">Message</label>
        <textarea class="textarea" placeholder="e.g. Hello world"></textarea>
    </div>
      <button class="button my-button">Envoyer</button>

  </div>
</template>

<script>
export default {
  name: 'ContactForm',
  props: {
      msg: String
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
