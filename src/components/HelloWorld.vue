<template>
  <div class="hello-world">
    <p>{{ msg }}</p>
  </div>
</template>

<script>
export default {
  name: "hello-world",
  data() {
    return {
      msg: ""
    };
  },
  async created() {
    const response = await fetch(".netlify/functions/hello-world");
    if (response.ok) {
      const data = await response.text();
      this.msg = data;
    }
  }
};
</script>

<style></style>
