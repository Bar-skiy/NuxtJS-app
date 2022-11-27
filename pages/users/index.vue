<template>
  <section>
    <h2>{{ pageTitle }}</h2>
    <div class="block">
      <ul>
        <li v-for="user in users" :key="user.id">
          <a href="#" @click.prevent="goTo(user)"
            >{{ user.name }} - ({{ user.email }})</a
          >
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
import { resolve } from "path";

export default {
  async fetch({ store, error }) {
    try {
      if (store.getters["users/users"].length === 0) {
      await store.dispatch("users/fetchUsers");
      }
    } catch (e) {
      error(e);
    }
  },

  data() {
    return {
      pageTitle: "Users page",
    };
  },

  computed: {
    users() {
      return this.$store.getters["users/users"];
    },
  },

  methods: {
    goTo(user) {
      this.$router.push("/users/" + user.id);
    },
  },
};
</script>