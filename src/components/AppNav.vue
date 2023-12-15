<template>
  <nav class="navbar navbar-expand-lg bg-success-subtle">
    <div class="container">
      <span class="navbar-brand">Blog</span>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#Content"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="Content">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <div v-for="menuItem in menuItems">
            <li class="nav-item" v-if="menuItem.isLoggedIn">
              <router-link class="nav-link" :to="menuItem.to">{{
                menuItem.title
              }}</router-link>
            </li>
          </div>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { computed } from "@vue/reactivity";

const menuItems = computed(() => {
  return [
    {
      title: "Nyitó oldal",
      to: "/",
      isLoggedIn: true,
    },
    {
      title: "Bejelentkezés",
      to: "/bejelentkezes",
      isLoggedIn: true,
    },
    {
      title: "Regisztráció",
      to: "/regisztracio",
      isLoggedIn: true,
    },
  ];
});
</script>

<style lang="scss" scoped></style>
