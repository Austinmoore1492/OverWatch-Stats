<template>
  <div>
    <Header />
    <div class="container">
      <router-view />
    </div>
    <p class="footer-paragraph">Powered By https://tracker.gg/</p>
  </div>
</template>

<script>
import Header from "./components/Header";
export default {
  name: "app",
  components: {
    Header
  }
};
</script>

<style>
:root {
  --primary-color: #405275;
}
@import url("https://fonts.googleapis.com/css?family=Poppins&display=swap");

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  background: var(--primary-color);
  font-family: "Poppins", Arial, Helvetica, sans-serif;
  color: #f0f0f0;
  line-height: 1.6;
}

a {
  color: #fff;
  text-decoration: none;
}

ul {
  list-style: none;
}

.body-bg-no-image {
  background: var(--primary-color);
}

.body-bg-image {
  background: var(--primary-color) url("./assets/tracer.png") no-repeat top
    center;
}

.container {
  width: 70%;
  margin: 1rem auto;
  overflow: auto;
  padding: 0 2rem;
}

.form-group {
  margin: 1rem 0;
}
.search {
  background: rgba(0, 0, 0, 0.7);
  border: 4px #fff solid;
  margin-top: 1rem;
  padding: 2rem;
}

input,
select,
textarea {
  display: block;
  width: 100%;
  padding: 0.4rem;
  font-size: 1.2rem;
  border: 1px solid #ccc;
}

.btn {
  background: var(--primary-color);
  color: #fff;
  padding: 0.4rem 1.3rem;
  border: none;
  border-radius: 4px;
  max-width: 50%;
  cursor: pointer;
  outline: none;
  margin: auto;
  margin-top: 1rem;
}

.footer-paragraph {
  position: absolute;
  bottom: 2%;
  left: 2%;
}

@media (max-width: 800px) {
  body {
    background: var(--primary-color);
  }
  .body-bg-image {
    background: var(--primary-color);
  }
  .container {
    width: 100%;
  }
  .footer-paragraph {
    display: none;
  }
}
</style>
