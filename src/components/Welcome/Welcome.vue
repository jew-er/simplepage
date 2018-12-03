<template>
  <section class="welcome">
    <div class="greeting">
      <span class="header">
        WE
        <b>LOVE</b> TO WRITE CODE
      </span>
      <div class="divider"></div>
      <div class="details">Lorem ipsum something something</div>
    </div>
    <div class="controls">
      <div class="wrapper">
        <img src="@/assets/welcome-play.png">
      </div>
      <div class="wrapper">
        <img src="@/assets/welcome-audio.png">
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Welcome"
};
</script>

<style lang="scss" scoped>
$orange: rgb(218, 73, 28);
.welcome {
  background-image: url("../../assets/bg-parallax.png");
  background-size: cover;
  width: 100%;
  height: 51vw;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;

  .greeting {
    color: white;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 64px;
    height: 70%;

    .header {
      font-size: 60px;
      font-family: "Open Sans", sans-serif;
      border-right: 3px solid rgba(255, 255, 255, 0.5);
      padding-left: 20px;
      padding-right: 20px;
      box-sizing: border-box;
    }

    .divider {
      height: 3px;
      width: 150px;
      background: $orange;
      margin-top: 50px;
      margin-bottom: 50px;
    }
    .details {
      font-size: 16px;
      font-family: "Lato", sans-serif;
      color: rgb(254, 253, 253);
    }
  }
  .controls {
    display: flex;
    justify-content: flex-end;
    width: 100%;
    padding: 30px;
    box-sizing: border-box;
    .wrapper {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      background: rgba(51, 51, 51, 0.25);
      margin: 2px;
      cursor: pointer;
      display: flex;
      justify-content: center;
      align-items: center;
    }
  }
}

@media only screen and (max-width: 800px) {
  .welcome {
    .greeting {
      .header {
        font-size: 30px;
      }
    }
    .controls {
      padding: 0;
      padding-bottom: 10px;
      padding-right: 10px;
      justify-content: flex-end;
    }
  }
}

@media only screen and (max-width: 500px) {
  .welcome {
    justify-content: space-around;
    align-items: flex-start;
    .greeting {
      margin: 0;
      width: 70%;
      .header {
        font-size: 20px;
        padding: 0;
        border: none;
      }
      .divider {
        display: none;
      }
    }
    .controls {
      padding: 0;
      padding-bottom: 10px;
      padding-right: 10px;
      justify-content: flex-end;
    }
  }
}
</style>
