<template>
  <section>
    <h2>Users page</h2>
    <div class="block">
    <ul>
      <li v-for="user in users" :key="user">
        <a href="#" @click.prevent="goTo(user)">User {{user}}</a>
      </li>
    </ul>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      users: [1, 2, 3, 4, 5],
    };
  },
  methods: {
    goTo(user) {
    this.$router.push('/users/' + user)
    }
  }
};
</script>