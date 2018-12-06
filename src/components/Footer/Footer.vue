<template>
  <footer class="footer">
    <div class="leftbox">
      <div class="row">
        <a href="#">OUR SPECIALTY</a>
        <a href="#">MEET OUR TEAM</a>
        <a href="#">HOW WE DO IT</a>
        <a href="#">WORKS</a>
        <a href="#">NEWS & ARTICLES</a>
        <a href="#">CONTACT</a>
      </div>
      <div class="col">
        <div class="email">Email Address</div>
        <div class="divider"></div>
        <p>Subscribe duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p>
      </div>
      <div class="copyright">Copyright 2016 | All Rights Reserved</div>
    </div>
    <div class="rightbox">
      <h2>Front-end Test</h2>
      <p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p>
    </div>
  </footer>
</template>
<script>
export default {
  name: "Footer"
};
</script>
<style lang="scss" scoped>
.footer {
  background-color: rgb(41, 41, 41);
  width: 100%;
  height: 374px;
  display: flex;
  box-sizing: border-box;
  .leftbox {
    width: 70%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    padding: 70px;
    box-sizing: border-box;
    .row {
      display: flex;
      justify-content: space-between;
      padding-right: 100px;
      a {
        font-size: 13px;
        font-family: "Open Sans";
        color: rgb(255, 255, 255);
        text-decoration: none;
      }
    }
    .col {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      width: 100%;
      .email {
        font-size: 60px;
        font-family: "Open Sans";
        color: rgb(76, 75, 75);
      }
      .divider {
        background: rgb(106, 105, 105);
        height: 1px;
        width: 100%;
      }
      p {
        margin-top: 10px;
        font-size: 14px;
        font-family: "Open Sans";
        color: rgb(153, 153, 153);
      }
    }
    .copyright {
      font-size: 14px;
      font-family: "Open Sans";
      color: rgba(255, 255, 255, 0.2);
    }
  }

  .rightbox {
    width: 30%;
    height: 100%;
    display: flex;
    flex-direction: column;
    padding: 70px;
    box-sizing: border-box;
    h2 {
      font-size: 26px;
      font-family: "Open Sans";
      color: rgb(255, 255, 255);
    }
    p {
      font-size: 14px;
      font-family: "Open Sans";
      color: rgb(153, 153, 153);
      line-height: 2.143;
    }
  }
}

@media only screen and (max-width: 1200px) {
  .footer {
    .leftbox {
      .row {
        padding-right: 0;
      }
    }
  }
}

@media only screen and (max-width: 1000px) {
  .footer {
    .leftbox {
      padding: 40px;
    }

    .rightbox {
      padding: 40px;
    }
  }
}

@media only screen and (max-width: 800px) {
  .footer {
    .leftbox {
      padding: 40px;
      .row {
        flex-direction: column;
      }
    }

    .rightbox {
      padding: 40px;
    }
  }
}
@media only screen and (max-width: 700px) {
  .footer {
    height: auto;
    flex-direction: column;
    .leftbox {
      width: 100%;
      height: auto;
      .row {
        flex-direction: column;
      }
    }

    .rightbox {
      width: 100%;
      height: auto;
    }
  }
}
</style>
