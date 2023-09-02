<template>
  <h2>Список фильмов</h2>
  <input type="text" placeholder="Введите фильм" v-model="nameFilm" />
  <input type="text" placeholder="Оценка" v-model.number="scoreFilm" />
  <hr />
  <button @click="addFilmToList">AddFilm</button>
  <button @click="log">logFilm</button>
</template>

<script>
export default {
  data() {
    return {
      filmList: [],
      nameFilm: "",
      scoreFilm: "",
    };
  },
  methods: {
    addFilmToList() {
      this.filmList.push({ film: this.nameFilm, score: this.scoreFilm });
      this.nameFilm = "";
      this.scoreFilm = "";
    },
    log() {
      console.log(this.filmList);
    },
  },
};
</script>
