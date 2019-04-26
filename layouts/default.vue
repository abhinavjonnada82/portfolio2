<template>
  <div>
    <navbar></navbar>
    <nuxt/>
  </div>
</template>

<style>
html {
  font-family: "Source Sans Pro", "Helvetica Neue", Arial, sans-serif;
}
</style>

<script>
import Navbar from "../components/Navbar";

export default {
  components: {
    Navbar
  }
};
</script>