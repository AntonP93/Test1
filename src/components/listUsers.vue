<template>
  <ol>
    <li v-for="item in listUsers" v-bind:key="item.name">
      Имя:{{ item.name }} Пароль:{{ item.password }}
    </li>
  </ol>
</template>

<script>
export default {
  props: ["listUsers"],
  methods: {},
};
</script>
