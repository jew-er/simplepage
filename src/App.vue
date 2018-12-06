<template>
  <div id="app">
    <nav-bar/>
    <welcome/>
    <specialty/>
    <para/>
    <faq/>
    <testimonial/>
    <achievements/>
    <div style="width: 100%">
      <iframe
        width="100%"
        height="600"
        src="https://maps.google.com/maps?width=100%&height=600&hl=en&coord=45.6978634,23.3221789&q=1%20Grafton%20Street%2C%20Dublin%2C%20Ireland+(My%20Business%20Name)&ie=UTF8&t=&z=14&iwloc=B&output=embed"
        frameborder="0"
        scrolling="no"
        marginheight="0"
        marginwidth="0"
      >
        <a href="https://www.maps.ie/map-my-route/">Create a route on google maps</a>
      </iframe>
    </div>
    <contact/>
    <Footer/>

    <br>
  </div>
</template>

<script>
import navBar from "./components/Nav/Nav.vue";
import welcome from "./components/Welcome/Welcome.vue";
import Specialty from "./components/Specialty/Specialty.vue";
import Para from "./components/Para/Para.vue";
import Faq from "./components/faq/Faq.vue";
import Testimonial from "./components/Testimonial/Testimonial.vue";
import Achievements from "./components/Achievements/Achievements.vue";
import Contact from "./components/Contact/Contact.vue";
import Footer from "./components/Footer/Footer.vue";

export default {
  name: "app",
  components: {
    navBar,
    welcome,
    Specialty,
    Para,
    Faq,
    Testimonial,
    Achievements,
    Contact,
    Footer
  }
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=Open+Sans:400|Lato|Merriweather:300");
* {
  margin: 0;
  padding: 0;
}

#app {
  overflow: hidden;
  display: flex;
  flex-direction: column;
}
</style>
