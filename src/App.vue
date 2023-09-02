<template>
  <h1>Привет</h1>
  <add-film />
</template>

<script>
import AddFilm from "./components/addFilm.vue";
export default {
  name: "App",
  components: { AddFilm },
};
</script>
