<template>
  <section class="specialty">
    <div class="details">
      <div class="header">
        <h1>OUR SPECIALTY</h1>
        <p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p>
      </div>
      <p>Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur?</p>
      <p>Et harum quidem rerum facilis est et expedita distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod maxime placeat facere possimus,</p>
    </div>
    <div class="cards">
      <div class="wrap">
        <Card
          img="specialty-hammer.png"
          head="DEVELOPMENT"
          details="something Successful needs more something placeholder lazy to get one"
        />
      </div>
      <div class="wrap">
        <Card
          img="specialty-pen.png"
          head="UI/UX"
          details="something Successful needs more something placeholder lazy to get one"
        />
      </div>
      <div class="wrap">
        <Card
          img="specialty-speaker.png"
          head="SOCIAL MARKETING"
          details="something Successful needs more something placeholder lazy to get one"
        />
      </div>
      <div class="wrap">
        <Card
          img="specialty-sign.png"
          head="SYSTEM ARCHITECTURE"
          details="something Successful needs more something placeholder lazy to get one"
        />
      </div>
      <div class="wrap">
        <Card
          img="specialty-book.png"
          head="COPYWRITING"
          details="something Successful needs more something placeholder lazy to get one"
        />
      </div>
      <div class="wrap">
        <Card
          img="specialty-camera.png"
          head="PHOTOGRAPHY"
          details="something Successful needs more something placeholder lazy to get one"
        />
      </div>
    </div>
  </section>
</template>

<script>
import Card from "./Card.vue";
export default {
  name: "Specialty",
  components: {
    Card
  }
};
</script>

<style lang="scss" scoped>
$orange: rgb(218, 73, 28);
.specialty {
  width: 100%;
  height: 650px;
  display: flex;
  .details {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
    width: 45%;
    height: 100%;
    box-sizing: border-box;
    padding: 60px;
    padding-bottom: 100px;
    .header {
      box-sizing: border-box;
      padding-bottom: 50px;
      width: 100%;
      h1 {
        border-left: 3px solid $orange;
        padding-left: 20px;
        font-family: "Open Sans", sans-serif;
        font-size: 36px;
        margin-bottom: 20px;
        width: 100%;
      }
      p {
        font-family: "Merriweather", serif;
        color: rgb(51, 51, 51);
        line-height: 1.875;
        font-size: 16px;
        width: 100%;
      }
    }

    p {
      font-family: "Open Sans", sans-serif;
      color: rgb(51, 51, 51);
      line-height: 1.875;
      font-size: 14px;
      width: 100%;
    }
  }
  .cards {
    display: flex;
    flex-wrap: wrap;
    width: 55%;
    height: 100%;
    .wrap {
      width: calc(33% + 1% / 3);
      height: 50%;
    }
  }
}

@media only screen and (max-width: 950px) {
  .specialty {
    flex-direction: column;
    height: auto;
    .details {
      width: 100%;
      p {
        margin-top: 30px;
      }
    }

    .cards {
      width: 100%;
      min-height: 500px;
      height: 50vh;
    }
  }
}

@media only screen and (max-width: 550px) {
  .specialty {
    .cards {
      max-width: 100%;
      min-height: 0;
      flex-direction: column;
      height: 900px;
      .wrap {
        width: 50%;
        height: 300px;
      }
    }
  }
}
@media only screen and (max-width: 400px) {
  .specialty {
    .cards {
      max-width: 100%;
      min-height: 0;
      flex-direction: column;
      height: auto;
      flex-wrap: nowrap;
      .wrap {
        width: 100%;
        height: 300px;
      }
    }
  }
}
</style>
