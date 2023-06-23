<template>
  <header class="d-flex justify-content-center py-3 bg-dark">
    <nav class="nav nav-pills">
      <router-link to="/" class="nav-link" :class="{ active: !activeLink }" @click="setActiveLink(false)">
        Accueil
      </router-link>
      <router-link to="/produits" class="nav-link" :class="{ active: activeLink }" @click="setActiveLink(true)">
        Produits
      </router-link>
    </nav>
  </header>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    const activeLink = ref(false)

    const setActiveLink = (value) => {
      activeLink.value = value
    }

    return {
      activeLink,
      setActiveLink
    }
  }
}
</script>
