<template>
  <section class="testimonial">
    <blockquote>“Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ”</blockquote>
    <img class="source" src="@/assets/quotesource.png">
    <cite>Daniela Jacobs / Big Company, LLC</cite>
    <div class="arrows">
      <div>
        <img src="@/assets/uparrow.png">
      </div>
      <div>
        <img src="@/assets/downarrow.png">
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Testimonial"
};
</script>

<style lang="scss" scoped>
$orange: rgb(218, 73, 28);
.testimonial {
  background: rgb(240, 238, 238);
  width: 100%;
  height: 500px;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  padding-top: 50px;
  padding-bottom: 50px;
  box-sizing: border-box;
  blockquote {
    font-size: 18px;
    font-family: "Merriweather";
    color: rgb(51, 51, 51);
    line-height: 2;
    max-width: 750px;
    text-align: center;
  }
  cite {
    font-size: 14px;
    font-family: "Open Sans";
    color: rgb(102, 102, 102);
    line-height: 2.15;
  }
  .source {
    border-radius: 50%;
    width: 100px;
    height: 100px;
  }
  .arrows {
    display: flex;
    div {
      background-color: rgb(204, 204, 204);
      width: 24px;
      height: 24px;
      display: flex;
      align-items: center;
      justify-content: center;
      &:hover {
        background: $orange;
      }
    }
  }
}
</style>
