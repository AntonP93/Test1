<template>
  <div>
    <h3>Форма ввода</h3>
    <div>
      <div>
        <label>Имя:</label>
        <input type="text" v-model="name" />
      </div>
      <div>
        <label>Пароль:</label>
        <input type="text" v-model="password" />
      </div>
      <div>
        <button @click="login">Login</button>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: "",
      password: "",
    };
  },
  methods: {
    login() {
      this.$emit("login", {
        name: this.name,
        password: this.password,
      });
      this.name = "";
      this.password = "";
    },
  },
};
</script>
