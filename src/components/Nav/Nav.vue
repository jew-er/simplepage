<template>
  <nav>
    <div class="desktop-nav">
      <div class="logo" >
        Front-end Test
      </div>
      <div class="menu">
        <drop-down label="HOME" />
        <drop-down label="ABOUT" :dropdown=
        "[{text: 'item 1', url:'#'},
        {text: 'item 2', url:'#'},
        {text: 'item 3', url:'#'}]" />
        <drop-down label="WORK" :dropdown=
        "[{text: 'item 1', url:'#'},
        {text: 'item 2', url:'#'},
        {text: 'item 3', url:'#'}]" />
        <drop-down label="NEWS" />
        <drop-down label="CONTACT" />
      </div>
    </div>
    <div class="mobilenav" :class="{'mobilenav-open': menu}">
      <div class="heading">Navigation</div>
      <div class="menu">
        <a href="#"> Our Specialty </a>
        <a href="#"> Our template </a>
        <a href="#"> How We Do It </a>
        <a href="#"> Works</a>
        <a href="#"> Brands & Clients </a>
        <a href="#"> Blog</a>
        <a href="#"> Contact </a>
      </div>
    </div>
    <div v-on:click="openMenu" class="hamburger" :class="{'hamburger-animation': menu}">
      <div class="dash"></div>
      <div class="dash"></div>
      <div class="dash"></div>
    </div>
  </nav>
</template>

<script>
import dropDown from "./dropdown.vue";
export default {
  name: "navBar",
  components: {
    dropDown
  },
  data: function() {
    return {
      menu: false
    };
  },
  methods: {
    openMenu() {
      this.menu = !this.menu;
    }
  }
};
</script>

<style lang="scss" scoped>
$orange: rgb(218, 73, 28);
.desktop-nav {
  width: 100vw;
  position: fixed;
  font-size: 18px;
  font-family: "Raleway";
  color: rgb(255, 255, 255);
  top: 0;
  height: 62px;
  background: rgba(17, 18, 21, 0.75);

  display: flex;
  justify-content: space-between;
  padding-left: 50px;
  padding-right: 50px;
  box-sizing: border-box;
  .logo {
    width: 200px;
    height: 100%;
    box-sizing: border-box;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
    font-size: 1.4em;
  }
  .menu {
    display: flex;
    width: 40%;
    min-width: 500px;
    height: 100%;
    box-sizing: border-box;
    align-items: center;
    justify-content: space-around;
  }
}

.mobilenav {
  background: rgba(17, 18, 21, 0.9);
  overflow: hidden;
  position: fixed;
  top: 0;
  width: 100vw;
  height: 0;
  transition: height 0.1s ease-in;
  display: none;
  flex-direction: column;
  .heading {
    font-size: 26px;
    font-family: "Open Sans";
    color: rgb(255, 255, 255);
    width: 100%;
    height: 80px;
    box-sizing: border-box;
    padding-left: 50px;
    padding-top: 10px;
  }
  .menu {
    width: 100%;
    height: 70%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
    box-sizing: border-box;
    a {
      font-size: 26px;
      font-family: "Open Sans";
      color: rgb(255, 255, 255);
      text-decoration: none;
      &:hover {
        color: $orange;
      }
    }
  }
}

.mobilenav-open {
  height: 100vh;
}

.hamburger {
  display: none;
  width: 28px;
  height: 31px;
  position: fixed;
  right: 40px;
  top: 15px;
  z-index: 33;
  cursor: pointer;
  .dash {
    width: 100%;
    height: 2px;
    background: white;
    transition: 0.2s ease-in;
  }
}

.hamburger-animation {
  .dash:nth-child(1) {
    transform: rotate(45deg) translate(4px, 8px);
    height: 1px;
  }

  .dash:nth-child(2) {
    opacity: 0;
    transform: scale(0);
  }

  .dash:nth-child(3) {
    transform: rotate(-45deg) translate(4px, -8px);
    height: 1px;
  }
}
@media only screen and (max-width: 900px) {
  .desktop-nav {
    align-items: center;
    display: none;
    .menu {
      display: none;
    }
  }
  .mobilenav {
    display: flex;
  }
  .hamburger {
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
  }
}
</style>
