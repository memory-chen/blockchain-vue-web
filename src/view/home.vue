<template>
  <div id="home">
    <mu-flexbox class="mt8" orient="vertical">
      <mu-flexbox-item order="0" class="flex-demo header-box">
        <my-header></my-header>
        <user-info></user-info>
        <tab-navs></tab-navs>
      </mu-flexbox-item>
      <mu-flexbox-item order="2" class="flex-demo" id='content-view'>
        <router-view></router-view>
      </mu-flexbox-item>
    </mu-flexbox>
  </div>
</template>

<script>
  import MyHeader from '@/components/Header'
  import UserInfo from '@/components/UserInfo'
  import TabNavs from '@/components/TabNavs'
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
      MyHeader,
      UserInfo,
      TabNavs
    }
  }
</script>

<style scoped>
  .header-box {
    height: 7rem;
    background: rgba(40, 38, 50, 1);
  }
</style>
