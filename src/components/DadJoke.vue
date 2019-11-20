<template>
  <div class="jokes">
    <p>{{ joke }}</p>
  </div>
</template>

<script>
export default {
  name: "dad-joke",
  data() {
    return {
      joke: ""
    };
  },
  async created() {
    const response = await fetch(".netlify/functions/node-fetch");
    if (response.ok) {
      const data = await response.json();
      this.joke = data.msg;
    }
  }
};
</script>

<style></style>
