<template>
  <section class="faq">
    <div class="video">
      <div>
        <img src="@/assets/faq-play.png">
      </div>
    </div>
    <div class="details">
      <h1>Commonly Asked Questions</h1>
      <div class="question">
        <div class="name">
          <div class="icon">+</div>
          <span>Is this design too lazy to use lorem ipsum placeholders?</span>
        </div>
        <div class="answer">Absolutely</div>
      </div>
      <div class="question">
        <div class="name">
          <div class="icon">+</div>
          <span>Who came up with the idea of lorem ipsum placeholders anyway?</span>
        </div>
        <div class="answer">Somebody whose name should be taboo to utter</div>
      </div>
      <div class="question">
        <div class="name">
          <div class="icon">+</div>
          <span>If not lorem ipsum, then what?</span>
        </div>
        <div
          class="answer"
        >Something that doesn't force you to look for it on the internet, like this text</div>
      </div>
      <div class="question">
        <div class="name">
          <div class="icon">+</div>
          <p>Can I hear a stupid joke?</p>
        </div>
        <div class="answer">To be Frank, I have to change my name</div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Faq"
};
</script>

<style lang="scss" scoped>
$orange: rgb(218, 73, 28);
.faq {
  display: flex;
  .video {
    background-image: url("../../assets/videobg.png");
    background-size: cover;
    //background-position: 50% 50%;
    width: 56.6%;
    height: 37vw;
    display: flex;
    align-items: center;
    justify-content: center;
    div {
      display: flex;
      align-items: center;
      justify-content: center;
      border: 1px solid white;
      border-radius: 50%;
      width: 60px;
      height: 60px;
      transform: translate(-5px, 5px);
      img {
        transform: translateX(2px);
      }
    }
  }

  .details {
    display: flex;
    flex-direction: column;
    padding-left: 30px;
    justify-content: center;
    h1 {
      font-size: 26px;
      font-family: "Open Sans";
      color: black;
    }

    .question {
      display: flex;
      flex-direction: column;
      .name {
        display: flex;
        align-items: center;
        font-size: 16px;
        font-family: "Open Sans";
        color: rgb(51, 51, 51);
        border-bottom: 1px solid rgba(51, 51, 51, 0.3);
        padding-bottom: 15px;
        margin-bottom: 15px;
        .icon {
          background: rgba(50, 50, 50, 0.25);
          color: white;
          border-radius: 50%;
          width: 30px;
          height: 30px;
          font-size: 2em;
          font-weight: bold;
          display: flex;
          vertical-align: center;
          text-align: center;
          align-items: center;
          justify-content: center;
          transition: transform 0.2s ease-in, background 0.2s ease-in;
          transform-origin: 50% 50%;
          padding-bottom: 3px;
          box-sizing: border-box;
          margin-right: 10px;
        }
        p {
          font-size: 14px;
          font-family: "Open Sans";
          color: rgb(102, 102, 102);
          line-height: 1.714;
          transition: color 0.2s ease-in;
        }
      }

      .answer {
        height: 0px;
        overflow: hidden;
        transition: height 0.2s ease-in;
        font-size: 14px;
        font-family: "Open Sans";
        color: rgb(102, 102, 102);
        line-height: 1.714;
      }
      &:hover {
        .name {
          p {
            color: $orange;
          }
          .icon {
            transform: rotate(45deg);
            background: $orange;
          }
        }
        .answer {
          height: 50px;
        }
      }
    }
  }
}
@media only screen and (max-width: 1000px) {
  .faq {
    flex-direction: column;
    .video {
      width: 100%;
      height: 56vw;
    }

    .details {
      width: 100%;
      height: auto;
    }
  }
}
</style>
