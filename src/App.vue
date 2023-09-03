<template>
  <login-form @login="addUser" />
  <hr />
  <list-users :listUsers="listUsers" />
</template>

<script>
import ListUsers from "./components/listUsers.vue";
import LoginForm from "./components/LoginForm.vue";
export default {
  name: "App",
  components: { LoginForm, ListUsers },
  data() {
    return {
      listUsers: [],
    };
  },
  created: function () {
    const userListDate = localStorage.getItem("user-list");
    if (userListDate) {
      this.listUsers = JSON.parse(userListDate);
    }
  },
  methods: {
    addUser(data) {
      this.listUsers = [...this.listUsers, data];
    },
  },
  watch: {
    listUsers() {
      localStorage.setItem("user-list", JSON.stringify(this.listUsers));
    },
  },
};
</script>
