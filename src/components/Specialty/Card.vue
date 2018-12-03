<template>
  <div class="card">
    <img :src=" require('@/assets/'+img)">
    <h3>{{head}}</h3>
    <p>{{details}}</p>
    <div class="chain">
      <img src="@/assets/specialty-chain.png">
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    img: String,
    head: String,
    details: String
  }
};
</script>

<style lang="scss" scoped>
.card {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  transition: background 0.2s ease-in, color 0.2s ease-in, padding 0.2s ease-in;
  height: 100%;
  font-family: "Open Sans", sans-serif;
  color: rgba(17, 18, 21, 0.75);
  box-sizing: border-box;
  width: 100%;
  padding-top: 50%;
  border: solid 1px rgb(204, 204, 204);

  h3 {
    font-size: 14px;
  }
  img {
    width: 34px;
    height: 34px;
  }
  p {
    text-align: center;
    font-size: 13px;
    line-height: 1.538;
    padding-left: 30px;
    padding-right: 30px;
    opacity: 0;
    transition: opacity 0.2s ease-in, transform 0.2s ease-in;
  }
  .chain {
    background: rgb(218, 73, 28);
    display: flex;
    justify-content: center;
    align-items: center;
    height: 0px;
    overflow: hidden;
    width: 100%;
    transition: height 0.2s ease-in;
    img {
      width: 24px;
      height: 24px;
    }
  }

  &:hover {
    background: rgb(41, 41, 41);
    color: White;
    padding-top: 30%;
    p {
      color: rgb(153, 153, 153);
      opacity: 1;
    }
    .chain {
      height: 50px;
    }
  }
}
</style>
