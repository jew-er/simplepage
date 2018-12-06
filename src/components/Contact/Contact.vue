<template>
  <section class="contact">
    <div class="info">
      <h1>CONTACT US</h1>
      <p>Quis autem vel eum molestiae consequatur, eum fugiat quo voluptas nulla pariatur?</p>
      <div class="con">
        <h3>HEADQUARTERS</h3>
        <p>123 W. Mission Blvd.</p>
        <p>Suite 101-191</p>
        <p>Pomona,CA.91766</p>
      </div>
      <div class="con">
        <h3>GET IN TOUCH</h3>
        <div>
          <font-awesome-icon icon="phone"/>
          <p>213-123-4567</p>
        </div>
        <div>
          <font-awesome-icon :icon="['fab', 'skype']"/>
          <p>USERID</p>
        </div>
        <div>
          <font-awesome-icon icon="envelope"/>
          <p>email@domain.com</p>
        </div>
      </div>
    </div>
    <form>
      <div class="row">
        <div class="input">
          <label>Full Name</label>
          <input>
        </div>
        <div class="input">
          <label>Email</label>
          <input>
        </div>
      </div>
      <div class="row">
        <div class="input">
          <label>What's your budget?</label>
          <input>
        </div>
        <div class="input">
          <label>Services you're inquiring about</label>
          <input>
        </div>
      </div>
      <div class="textarea">
        <label>Tell us about your project</label>
        <textarea rows="8"></textarea>
      </div>
      <button>SEND MESSAGE</button>
    </form>
  </section>
</template>
<script>
export default {
  name: "Contact"
};
</script>
<style lang="scss" scoped>
.contact {
  width: 100%;
  height: 540px;
  background-color: rgb(240, 238, 238);
  display: flex;

  .info {
    display: flex;
    flex-direction: column;
    box-sizing: border-box;
    padding: 60px;
    padding-top: 40px;
    padding-bottom: 140px;
    justify-content: space-between;
    height: 100%;
    width: 40%;
    h1 {
      font-size: 36px;
      font-family: "Open Sans";
      color: rgb(0, 0, 0);
      text-transform: uppercase;
      padding-left: 20px;
      border-left: 3px solid rgb(130, 130, 130);
    }
    p {
      font-size: 16px;
      font-family: "Merriweather";
      color: rgb(51, 51, 51);
      margin-bottom: 20px;
    }

    .con {
      h3 {
        font-size: 14px;
        font-family: "Raleway";
        color: rgb(0, 0, 0);
        margin-bottom: 10px;
      }
      p {
        font-size: 14px;
        font-family: "Lato";
        color: rgb(50, 50, 50);
        margin-bottom: 3px;
      }
      div {
        display: flex;
        margin-bottom: 3px;
      }
      div p {
        font-size: 14px;
        font-family: "Lato";
        color: rgb(50, 50, 50);
        margin-left: 5px;
      }
    }
  }
  form {
    width: 60%;
    padding: 20px;
    box-sizing: border-box;
    .row {
      display: flex;
      .input {
        display: flex;
        flex-direction: column;
        width: 50%;
        box-sizing: border-box;
        padding: 20px;
        label {
          font-size: 14px;
          font-family: "Open Sans";
          color: rgb(51, 51, 51);
        }
        input {
          border-style: solid;
          border-width: 1px;
          border-color: rgb(204, 204, 204);
          background-color: rgb(255, 255, 255);
          height: 49px;
        }
      }
    }
    .textarea {
      padding: 20px;
      box-sizing: border-box;
      width: 100%;
      display: flex;
      flex-direction: column;
      label {
        font-size: 14px;
        font-family: "Open Sans";
        color: rgb(51, 51, 51);
      }

      textarea {
        resize: vertical;
        border-style: solid;
        border-width: 1px;
        border-color: rgb(204, 204, 204);
        background-color: rgb(255, 255, 255);
      }
    }
    button {
      border-radius: 3px;
      background-color: rgb(41, 41, 41);
      position: absolute;
      width: 189px;
      height: 49px;
      font-size: 14px;
      font-family: "Open Sans";
      color: rgb(255, 255, 255);
      transition: background 0.1s ease-in;
      margin-left: 20px;
      border: none;
      cursor: pointer;
      &:hover {
        background: rgb(90, 90, 90);
      }
    }
  }
}

@media only screen and (max-width: 1000px) {
  .contact {
    flex-direction: column;
    height: auto;
    align-items: center;
    justify-content: space-between;
    padding-bottom: 50px;
    .info {
      width: 100%;
      flex-direction: row;
      flex-wrap: wrap;
      height: auto;
    }
    form {
      width: 100%;
      height: auto;
    }
  }
}

@media only screen and (max-width: 500px) {
  .contact {
    box-sizing: border-box;

    .info {
      padding-bottom: 0;
    }
    form {
      .row {
        flex-direction: column;
        .input {
          width: 100%;
        }
      }
    }
  }
}
</style>
