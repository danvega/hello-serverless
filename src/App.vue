<template>
  <div id="app">
    <h1>Hello, Serverless</h1>
    <hello-world />
    <dad-joke />
  </div>
</template>

<script>
import HelloWorld from "@/components/HelloWorld";
import DadJoke from "@/components/DadJoke";

export default {
  components: {
    HelloWorld,
    DadJoke
  }
};
</script>
