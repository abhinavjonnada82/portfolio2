<template>
  <section class="section">
    <div class="container">
      <img
        src="https://render.bitstrips.com/v2/cpanel/fb695398-7ef1-4461-987b-73d3a97805fd-8f6667c1-8cb6-4fd0-9394-de53c0e28b19-v1.png?transparent=1&palette=1"
        class="avatar-img"
      />
      <hr />
      <div class="title-text">
        <h1 class="title">I'm Abhinav Jonnada</h1>
        <h2 class="subtitle">Software Engineer ⚙️ & Technology Enthusiast</h2>
      </div>

      <hr />

      <p class="banner-text">
        “Yesterday is history, tomorrow is a mystery, and today is a gift... that's why they call it present”
        ― Master Oogway 🐼
      </p>
    </div>
    <br />
    <footer>
      Powered by
      <i class="fab fa-vuejs"></i>. ©️ 2019 Abhinav Jonnada
    </footer>
  </section>
</template>

<style>
footer {
  display: block;
  text-align: center;
}
.banner-text {
  text-align: center;
}
.title-text {
  text-align: center;
}
.template {
  background: require(
    "https://www.freepik.com/free-vector/memphis-pattern_1177561.htm"
  );
  background-size: cover;
  height: 500px;
  position: relative;
}
img {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 300px;
}
</style>

<script>
import AppLogo from "~/components/AppLogo.vue";

export default {
  components: {
    AppLogo
  }
};
</script>

<style>
</style>

