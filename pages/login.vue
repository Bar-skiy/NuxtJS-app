<template>
  <form>
    <h1>login</h1>
    <div class="form-group">
      <input type="text" class="form-control" />
    </div>
    <div class="form-group">
      <input type="password" class="form-control" />
    </div>
    <button class="btn btn-primary">Login</button>
    <nuxt-link class="link" to="/">Home</nuxt-link>
  </form>
</template>

<script>
export default {
  layout: "empty",
};
</script>

<style scoped>
form {
  width: 600px;
}
input {
  margin-bottom: 15px;
  margin-top: 15px;
}
.link {
   margin-left: 480px; 
}

</style>