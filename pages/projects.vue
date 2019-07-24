<template>
  <section class="hero is-medium is-primary is-bold">
    <div class="hero-body">
      <div class="container">
        <h1 class="title">My Pojects</h1>
        <h2 class="subtitle">
          Projects are dynamically retrieved (too lazy to hard code my projects!) from GitHub using
          <i
            class="fab fa-github fa-3x"
            aria-hidden="true"
          /> API&nbsp;
          <b-switch type="is-warning" v-model="showRepos"></b-switch>
        </h2>
      </div>
      <br />
      <div v-for="x in wholeResponse" :key="x.id">
        <div class="card">
          <header class="card-header">
            <p class="card-header-title">{{x.name}}</p>
          </header>
          <div class="card-content">
            <div class="content">{{x.description}}</div>
          </div>
          <footer class="card-footer">
            <a :href="x.html_url" class="card-footer-item">View Repo</a>
          </footer>
        </div>
        <br />
      </div>
    </div>
  </section>
</template>


<script>
import axios from "axios";
import Vue from "vue";
import Buefy from "buefy";
import "buefy/dist/buefy.css";

Vue.use(Buefy);
export default {
  data() {
    return {
      wholeResponse: [],
      showProject: false,
      showRepos: null
    };
  },
  watch: {
    showRepos: async function() {
      axios
        .get(
          'https://api.github.com/users/abhinavjonnada82/starred?client_id= "Iv1.3b41e3643519b3c5" & client_secret="e3ceebf765f65d528f57a0f0579e6f7db6efcce4"'
        )
        .then(response => {
          this.wholeResponse = response.data;
          this.showProject = true;
        })
        .catch(error => {
          console.log(error);
        });
    }
  }
};
</script>
