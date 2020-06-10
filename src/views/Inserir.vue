<template>
  <v-card class="mx-auto" style="max-width: 500px;">
    <v-toolbar color="deep-purple accent-4" cards dark flat>
      <v-card-title class="title font-weight-regular"
        >Adicionar Portaria</v-card-title
      >
      <v-spacer></v-spacer>
    </v-toolbar>
    <v-form ref="form" v-model="form" class="pa-4 pt-6">
      <v-text-field
        v-model="titulo"
        :rules="[rules.titulo]"
        filled
        color="deep-purple"
        label="Portaria"
        style="min-height: 96px"
      ></v-text-field>
      <v-textarea
        v-model="descricao"
        auto-grow
        :rules="[rules.required]"
        filled
        color="deep-purple"
        label="Descrição"
        rows="5"
      ></v-textarea>
      <v-file-input :rules="[rules.arquivo]" label="Selecionar portaria"></v-file-input>
    </v-form>
    <v-divider></v-divider>
    <v-card-actions>
      <v-spacer></v-spacer>
      <v-btn
        :disabled="!form"
        class="white--text"
        color="deep-purple accent-4"
        depressed
        >Enviar</v-btn
      >
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    form: false,
    titulo: undefined,
    descricao: undefined,
    arquivo: undefined,
    rules: {
      required: (v) => !!v || "Descrição necessaria",
      titulo: (v) => !!v || "Texto Necessario",
      arquivo: (v) => !!v || "Arquivo Necessario",
    },
  }),
};
</script>
