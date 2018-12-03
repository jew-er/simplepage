<template>
  <section class="para">
    <div class="details">
      <h3>CLEAN & MODERN DESIGN + PARALAX EFFECT FOR IMG.</h3>
      <div class="divider"></div>
      <h1>LOOKS TERRIBLE ON MOBILE DEVICES</h1>
      <div class="buttons">
        <a href="#">
          <div>CONTACT US</div>
        </a>
        <a href="#">
          <div>LEARN MORE</div>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Para"
};
</script>

<style lang="scss" scoped>
$orange: rgb(218, 73, 28);
.para {
  background-image: url("../../assets/Parallaxbg.png");
  background-size: cover;
  background-position: 50% 50%;
  width: 100%;
  height: 40vw;
  box-sizing: border-box;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  .details {
    width: 60%;
    height: 60%;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: flex-start;
    padding-left: 75px;
    h3 {
      font-size: 26px;
      font-family: "Open Sans", sans-serif;
      color: rgb(255, 255, 255);
      line-height: 1.385;
    }
    h1 {
      font-size: 55px;
      font-family: "Open Sans";
      color: rgb(255, 255, 255);
      line-height: 1;
      width: 70%;
    }
    .divider {
      background: $orange;
      width: 85px;
      min-height: 3px;
    }
    .buttons {
      display: flex;
      width: 70%;
      a {
        text-decoration: none;
        color: white;
        &:nth-child(2) {
          margin-left: 10px;
        }
        div {
          display: flex;
          align-items: center;
          justify-content: center;
          width: 220px;
          height: 50px;
          font-family: "Lato";
          border-radius: 4px;
          background: rgb(50, 50, 50);
          color: white;
          transition: background 0.2s ease-in;
          font-size: 14px;
          &:hover {
            background: $orange;
          }
        }
      }
    }
  }
}

@media only screen and (max-width: 1200px) {
  .para {
    .details {
      h1 {
        font-size: 33px;
      }
      h3 {
        font-size: 20px;
      }
    }
  }
}

@media only screen and (max-width: 960px) {
  .para {
    .details {
      h1 {
        font-size: 25px;
      }
      h3 {
        font-size: 15px;
      }

      .buttons {
        a {
          div {
            width: 150px;
          }
        }
      }
    }
  }
}
@media only screen and (max-width: 740px) {
  .para {
    height: 70vw;
    .details {
      padding-left: 10px;
      h1 {
        font-size: 12px;
      }
      h3 {
        font-size: 12px;
      }

      .divider {
        display: none;
      }
      .buttons {
        flex-direction: column;
        a {
          &:nth-child(2) {
            margin: 0;
            margin-top: 5px;
          }
          div {
            width: 120px;
            margin: 0;
          }
        }
      }
    }
  }
}
</style>
