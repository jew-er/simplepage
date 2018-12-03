<template>
  <div class="item">
    <p class="item-label">
      {{label}}
    </p>
    <div class="item-dropdown" >
      <a v-for="(i,key) in dropdown" v-bind:key = "key" :href="i.url">{{i.text}}</a>
    </div>
  </div>
</template>
<script>
export default {
  name: "dropdown",
  props: {
    label: String,
    dropdown: Array
  }
};
</script>


<style lang="scss" scoped>
$orange: rgb(218, 73, 28);
.item {
  height: 100%;
  .item-label {
    cursor: pointer;
    font-weight: bold;
    transition: color 0.1s ease-in;
    font-size: 18px;
    height: 100%;
    display: flex;
    align-items: center;

    &:hover {
      color: $orange;
    }
  }
  .item-dropdown {
    position: fixed;
    top: 62px;
    display: flex;
    flex-direction: column;
    background: rgb(17, 18, 21);
    transform: scaleY(0) translateX(-20px);
    opacity: 0;
    height: auto;
    overflow: hidden;
    box-sizing: border-box;
    transition: transform 0.1s ease-in, opacity 0.1s ease-in;
    line-height: 2em;
    transform-origin: 50% 0;

    a {
      text-decoration: none;
      color: white;
      font-size: 18px;
      margin-right: 110px;
      margin-left: 20px;
      &:hover {
        color: $orange;
      }
      &:first-child {
        margin-top: 20px;
      }
      &:last-child {
        margin-bottom: 30px;
      }
    }
  }
  &:hover {
    .item-dropdown {
      transform: scaleY(1) translateX(-20px);
      opacity: 1;
    }
  }
}
</style>
