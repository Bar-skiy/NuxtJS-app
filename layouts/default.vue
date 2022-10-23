<template>
  <div>
    <Navbar />
    <main>
      <div class="container text-center">
        <Nuxt />
      </div>
    </main>
  </div>
</template>
<script>
import Navbar from "@/components/Navbar.vue";
export default {
  components: {
    Navbar,
  },
};
</script>