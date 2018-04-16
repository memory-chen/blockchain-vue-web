<template>
  <div id="home">
    <mu-flexbox class="mt8" orient="vertical">
      <mu-flexbox-item order="0" class="flex-demo header-box">
        <my-header></my-header>
      </mu-flexbox-item>
      <mu-flexbox-item order="2" class="flex-demo">
        10
      </mu-flexbox-item>
    </mu-flexbox>
  </div>
</template>

<script>
  import MyHeader from '@/components/Header'
  export default {
    data() {
      return {
        name: 'value'
      }
    },
    methods: {
      a() {
        console.log(111)
      }
    },
    components: {
      MyHeader
    }
  }
</script>

<style scoped>
  .header-box {
    height: 7rem;
    background: rgba(40, 38, 50, 1);
  }
</style>
