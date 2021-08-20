<script>
export default {
  name: "Navbar",
  props: ["name", "logoImage", "navLinks"],
  methods: {
    closeNavbar() {
      const burger = document.querySelector(".hamburger");
      const navLinks = document.querySelector(".nav__links");

      navLinks.classList.toggle("nav-active");
      burger.classList.toggle("toggle");
    },
    toggleNavbar() {
      const burger = document.querySelector(".hamburger");
      const navLinks = document.querySelector(".nav__links");
      const navLink = document.querySelectorAll(".nav__links li");

      navLinks.classList.toggle("nav-active");
      burger.classList.toggle("toggle");
      navLink.forEach((link, index) => {
        if (link.style.animation || link.style.webkitAnimation) {
          link.style.animation = "";
          link.style.webkitAnimation = "";
        } else {
          link.style.webkitAnimation = `navLinkFade 0.5s ease forwards ${
            index / 7
          }`;
          link.style.animation = `navLinkFade 0.5s ease forwards ${index / 7}`;
        }
      });
    },
  },
};
</script>

<template>
  <nav>
    <div class="logo">
      <h2>STAR WARS</h2>
    </div>
    <ul class="nav__links">
      <li v-for="item in navLinks" @click="closeNavbar()" :key="item.key">
        <router-link :to="item.path">{{ item.name }}</router-link>
      </li>
    </ul>
    <div class="hamburger" @click="toggleNavbar()">
      <div class="line1"></div>
      <div class="line2"></div>
      <div class="line3"></div>
    </div>
  </nav>
</template>

<style scoped lang="scss">
nav {
  /* use icons instead, have active icon hover animation */
  height: 100%;
  width: 100%;
  background: #f8f8f8;
  padding: 2rem;
  z-index: 5;
  position: relative;
  display: flex;
  justify-content: space-between;
  align-items: center;
  /* margin-bottom: 2em; */

  a {
    text-decoration: none;
    text-transform: uppercase;
    color: rgb(12, 12, 12);
    &.router-link-exact-active {
      color: crimson;
    }
  }

  .nav__links {
    display: flex;
    width: 40%;
    /* background: green; */
    gap: 1em;
    list-style-type: none;
  }
  .hamburger {
    flex-direction: column;
    gap: 0.5em;
    display: none;
    &.toggle {
      color: crimson;
      .line1 {
        transform: rotate(-45deg) translate(-9px, 10px);
      }
      .line2 {
        opacity: 0;
      }
      .line3 {
        transform: rotate(45deg) translate(-5px, -6px);
      }
    }
    div {
      height: 3px;
      width: 30px;
      background-color: #1a1a1a;
    }
  }
}

@keyframes navLinkFade {
  from {
    opacity: 0;
    transform: translateX(-60px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@media (min-width: 1024px) {
  nav .nav__links {
    width: 30%;
  }
}

@media (max-width: 768px) {
  nav {
    a {
      color: #fff;
    }
    .nav__links {
      overflow: hidden;
      position: absolute;
      flex-direction: column;
      padding: 2em 0;
      width: 100%;
      background: rgb(20, 20, 20);
      top: 100%;
      left: -100%;
      /* right: 0; */
      transition: left 200ms ease-in-out, opacity 55ms ease-in;
      opacity: 0;
      border-bottom-right-radius: 10px;
      border-bottom-left-radius: 10px;
      &.nav-active {
        left: 0;
        box-shadow: 4px 4px 4px rgba(0, 0, 0, 0.3);
        opacity: 1;
      }
    }
    .hamburger {
      display: flex;
      flex-direction: column;
    }
  }
}
</style>