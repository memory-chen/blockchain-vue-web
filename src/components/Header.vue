<template>
  <p id="header">
    <mu-badge content="" class="demo-icon-badge" circle secondary>
      <mu-icon value="message" />
    </mu-badge>
  </p>
</template>

<script>
  export default {
    name: 'header'
  }
</script>

<style lang='less'>
  #header {
    color: aliceblue;
    padding: 0 10px;
    font-size: 1rem;
    margin: 0px;
    .mu-badge-circle {
      border-radius: 50%;
      padding: 0;
      width: 10px;
      height: 10px;
      overflow: hidden;
    }
    .mu-badge-float {
      position: absolute;
      top: 16px;
      right: 0px;
    }
  }
</style>
