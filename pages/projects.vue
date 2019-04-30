<template>
  <section class="section is-medium">
    <div class="container has-text-centered">
      <h1 class="title">My Projects</h1>
      <p>
        My projects can be found on
        <a
          href="https://github.com/abhinavjonnada82"
          target="_blank"
        >GitHub</a>.
        <button @click="gitRepos">View</button>
        <br>
      </p>
    </div>
  </section>
</template>


<script>
export default {
  data() {
    return {
      client_id: "Iv1.3b41e3643519b3c5",
      client_secret: "e3ceebf765f65d528f57a0f0579e6f7db6efcce4"
    };
  },
  methods: {
    gitRepos: async function() {
      const api_call = await fetch(`https://api.github.com/users/abhinavjonnada82/starred?client_id=this.client_id&
        client_secret=this.client_secret`);
      const data = await api_call.json();
      return { data };
      console.log(data);
      console.log("Hello World!");
    }
  }
};
</script>