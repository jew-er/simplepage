<template>
  <section class="achievements">
    <div class="details">
      <h3 class="title">Solving Problems and Keeping Clients Happy</h3>
      <p
        class="para"
      >Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p>
      <div class="counter">
        <div class="counter-item">
          <img src="@/assets/commits.png">
          <div>
            <h1>886</h1>
            <p>commits</p>
          </div>
        </div>
        <div class="counter-item">
          <img src="@/assets/happy.png">
          <div>
            <h1>68+</h1>
            <p>Happy Clients</p>
          </div>
        </div>
        <div class="counter-item">
          <img src="@/assets/bugs.png">
          <div>
            <h1>335</h1>
            <p>Bugs Fixed</p>
          </div>
        </div>
      </div>
    </div>
    <img class="person" src="@/assets/person.png">
  </section>
</template>

<script>
export default {
  name: "Achievements"
};
</script>

<style lang="scss" scoped>
$orange: rgb(218, 73, 28);
.achievements {
  background-image: url("../../assets/count-bg.png");
  background-size: cover;
  width: 100%;
  height: 485px;
  display: flex;
  .details {
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    width: 60%;
    height: 100%;
    box-sizing: border-box;
    padding-left: 70px;
    padding-top: 60px;
    padding-bottom: 60px;
    padding-right: 70px;
    .title {
      font-size: 26px;
      font-family: "Open Sans";
      color: rgb(255, 255, 255);
      font-weight: bold;
      line-height: 1.385;
    }
    .para {
      font-size: 14px;
      font-family: "Open Sans";
      color: rgb(255, 255, 255);
      line-height: 2.143;
    }
    .counter {
      display: flex;
      justify-content: space-between;
      .counter-item {
        display: flex;
        img {
          max-width: 50px;
          max-height: 44px;
          margin-right: 20px;
        }
        div {
          display: flex;
          flex-direction: column;
          justify-content: center;
          h1 {
            font-size: 60px;
            font-family: "Open Sans";
            line-height: 0.8em;
            color: rgb(255, 255, 255);
          }
          p {
            font-size: 24px;
            font-family: "Open Sans";
            color: rgb(255, 255, 255);
          }
        }
      }
    }
  }

  .person {
    min-height: 548px;
    transform: translateY(-63px);
  }
}

@media only screen and (max-width: 1185px) {
  .achievements {
    .details {
      width: 100%;
    }
    .person {
      display: none;
    }
  }
}

@media only screen and (max-width: 885px) {
  .achievements {
    .details {
      .counter {
        .counter-item {
          img {
          }
          div {
            h1 {
              font-size: 40px;
            }
            p {
              font-size: 15px;
            }
          }
        }
      }
    }
  }
}

@media only screen and (max-width: 580px) {
  .achievements {
    .details {
      padding: 15px 15px;
      .counter {
        .counter-item {
          img {
          }
          div {
            h1 {
            }
            p {
            }
          }
        }
      }
    }
  }
}

@media only screen and (max-width: 480px) {
  .achievements {
    .details {
      padding: 15px 15px;
      .counter {
        .counter-item {
          &:nth-child(1) {
            border-right: 2px solid white;
            padding-right: 5px;
          }
          &:nth-child(2) {
            border-right: 2px solid white;
            padding-right: 5px;
          }
          img {
            display: none;
          }

          div {
            text-align: center;
            h1 {
              font-size: 30px;
            }
          }
        }
      }
    }
  }
}
</style>
