<script setup>
import { ref } from "vue";
const form = ref({
  email: "",
  password: "",
});

function submit() {
  alert(JSON.stringify(form.value));
}
</script>

<template>
  <v-sheet class="mx-auto" width="300">
    <v-form @submit.prevent="submit">
      <v-text-field
        v-model="form.email"
        clearable
        label="Email"
        prepend-inner-icon="mdi-mail"
        variant="solo"
      ></v-text-field>
      <v-text-field
        v-model="form.password"
        clearable
        label="Password"
        type="password"
        prepend-inner-icon="mdi-key"
        variant="solo"
      ></v-text-field>
      <v-btn class="mt-2" type="submit" block>Submit</v-btn>
    </v-form>
  </v-sheet>
</template>
