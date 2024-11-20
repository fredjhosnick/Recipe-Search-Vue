<template>

  <AppHeader></AppHeader>
  <RecipeItem></RecipeItem>
  <router-view />
</template>

<script>
import AppHeader from '@/components/AppHeader.vue';

export default {
  components: {
    AppHeader,

  }
}

</script>

<style>
body {
  margin: 0;
}



input {
  border: 0;
  border-radius: 8px;
  width: 100%;
  outline: none;
  height: 30px;
}
</style>
