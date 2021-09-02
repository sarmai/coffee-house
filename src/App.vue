<template>
  <Navbar />
  <div class="page">
    <router-view />
  </div>
  <div class="footer">
    <Footer />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Footer,
  },
};
</script>

<style>
.page {
  padding: 0;
  margin-top: 12vh;
  overflow-x: hidden;
}

.footer {
  background-color: var(--primary);
  padding: 2em;
}

@media (min-width: 740px) {
  .footer {
    padding-right: 50%;
  }
}

@media (min-width: 970px) {
  .page {
    margin-top: 0;
    margin-left: 27vw;
  }

  .footer {
    display: none;
  }
}
</style>
