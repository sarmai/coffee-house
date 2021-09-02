<template>
  <nav class="navbar">
    <router-link to="/" class="nav-logo">GG Coffee</router-link>
    <ul :class="['nav-menu', { active: isActive }]">
      <li class="nav-item">
        <router-link to="/" class="nav-link" @click="closeMenu"
          >Home</router-link
        >
      </li>
      <li class="nav-item">
        <router-link to="/about" class="nav-link" @click="closeMenu"
          >About</router-link
        >
      </li>
      <li class="nav-item">
        <router-link to="/menu" class="nav-link" @click="closeMenu"
          >Menu</router-link
        >
      </li>
      <!-- <li class="nav-item">
        <router-link to="/reservations" class="nav-link" @click="closeMenu"
          >Reservations</router-link
        >
      </li> -->
      <li class="nav-item">
        <router-link to="/contact" class="nav-link" @click="closeMenu"
          >Contact</router-link
        >
      </li>
    </ul>
    <div :class="['hamburger', { active: isActive }]" @click="mobileMenu">
      <span class="bar"></span>
      <span class="bar"></span>
    </div>
    <Footer />
  </nav>
</template>

<script>
import Footer from "../components/Footer.vue";

export default {
  name: "Navbar",
  components: {
    Footer,
  },
  data() {
    return {
      isActive: false,
    };
  },
  methods: {
    mobileMenu() {
      this.isActive = !this.isActive;
    },
    closeMenu() {
      this.isActive = false;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.navbar {
  position: fixed;
  background: var(--primary) url(../assets/img/pink.jpg) no-repeat;
  background-size: cover;
  top: 0;
  left: 0;
  overflow: hidden;
  width: 27vw;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  padding: 2em 3em;
  z-index: 200;
  font-size: 1.3rem;
  letter-spacing: 0.15em;
}

.navbar li {
  list-style: none;
}

.navbar a {
  text-decoration: none;
}

.nav-menu {
  margin: 3em 0;
  padding: 0;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 1em;
  font-weight: 500;
  text-transform: uppercase;
}

.nav-logo {
  color: white;
  font-weight: 800;
  font-size: 2rem;
  border-bottom: none;
}

.nav-link {
  color: white;
}

.nav-link:hover,
.router-link-active:not(.nav-logo) {
  color: white;
  border-bottom: 2px solid white;
}

.hamburger {
  display: none;
}

.hamburger .bar {
  display: block;
  width: 40px;
  height: 3px;
  margin: 0.42em auto;
  -webkit-transition: all 0.3s ease-in-out;
  transition: all 0.3s ease-in-out;
  background-color: white;
}

@media (max-width: 970px) {
  .navbar {
    width: 100vw;
    height: 12vh;
    flex-direction: row;
    align-items: center;
    padding: 1em;
  }

  .nav-menu {
    position: fixed;
    margin: 0;
    padding: 3em;
    top: -100%;
    left: 0;
    height: 100vh;
    flex-direction: column;
    align-items: center;
    gap: 0.5em;
    width: 100%;
    text-align: center;
    transition: 0.3s;
    background-color: rgba(0, 0, 0, 0.8);
    box-shadow: 0 10px 27px rgba(0, 0, 0, 0.05);
    z-index: 99;
  }

  .nav-menu.active {
    top: 12vh;
  }

  .nav-item {
    margin: 0.8em 0;
  }

  /* .nav-link {
    color: var(--darkgrey);
  } */

  .hamburger {
    display: block;
    cursor: pointer;
  }

  .hamburger.active .bar:nth-child(1) {
    transform: translateY(6px) rotate(45deg);
  }

  .hamburger.active .bar:nth-child(2) {
    transform: translateY(-6px) rotate(-45deg);
  }

  .nav-footer {
    display: none;
  }
}
</style>
