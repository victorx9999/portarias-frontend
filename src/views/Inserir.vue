<template>
  <v-form>
    <v-divider></v-divider>
    <h1>Titulo</h1>
    <v-text-field
      label="Subject"
      value="Plans for the weekend"
      single-line
      full-width
      hide-details
    ></v-text-field>
    <v-divider></v-divider>
    <h1>Portaria</h1>
    <v-textarea
      v-model="title"
      label="Message"
      full-width
      single-line
    ></v-textarea>
  </v-form>
</template>

<script>
  export default {
    data () {
      return {
        selected: ['Trevor Handsen'],
        items: ['Trevor Handsen', 'Alex Nelson'],
        title: 'Hi,\nI just wanted to check in and see if you had any plans the upcoming weekend. We are thinking of heading up to Napa',
      }
    },
  }
</script>