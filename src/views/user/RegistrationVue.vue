<template>
  <div class="container mb-5">
    <div class="row">
      <div class="col-12">
        <h1 class="display-6 my-5 text-center">Regisztráció</h1>
      </div>
    </div>
    <div class="row">
      <div class="col-12 vol-md-4 mx-auto">
        <form @submit.prevent="onRegister">
          <div class="form-floating mb-3">
            <input
              type="text"
              class="form-control"
              id="name"
              placeholder="Név"
              v-model="regForm.name"
            />
            <label for="name">Név</label>
          </div>
          <div class="form-floating mb-3">
            <input
              type="text"
              class="form-control"
              id="email"
              placeholder="E-mail"
              v-model="regForm.email"
            />
            <label for="email">E-mail</label>
          </div>
          <div class="form-floating mb-3">
            <input
              type="password"
              class="form-control"
              id="password"
              placeholder="Jelszó"
              v-model="regForm.password"
            />
            <label for="password">Jelszó</label>
          </div>
          <div class="form-floating mb-3">
            <input
              type="password"
              class="form-control"
              id="passwordConfirmation"
              placeholder="Jelszó újra"
              v-model="regForm.passwordConfirmation"
            />
            <label for="passwordConfirmation">Jelszó újra</label>
          </div>
          <div class="mb-3">
            <button type="submit" class="btn btn-primary w-100 py-2">
              Regisztráció
            </button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const regForm = ref({
  name: "",
  email: "",
  password: "",
  passwordConfirmation: "",
  role: 0,
});

function onRegister() {
  console.log(regForm.value);
}
</script>

<style lang="scss" scoped></style>
