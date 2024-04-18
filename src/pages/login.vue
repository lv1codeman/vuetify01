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
  <v-card class="pa-4 mx-auto" width="300">
    <v-card-title class="text-center"> Login Here </v-card-title>
    <v-card-item>
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
        <v-btn class="mt-2" color="red-darken-1" type="submit" block
          >Submit</v-btn
        >
      </v-form>
    </v-card-item>
    <v-card-action>
      <div class="mx-4">
        <v-btn block to="/register">Register</v-btn>
      </div>
    </v-card-action>
  </v-card>
</template>
