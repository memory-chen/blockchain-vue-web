<template>
  <mu-paper id="navBar">
    <mu-bottom-nav :value="bottomNav" shift @change="handleChange">
      <mu-bottom-nav-item value="ACCOUNT/53" title="ACCOUNT/53" icon="account_box" >
      </mu-bottom-nav-item>
      <mu-bottom-nav-item value="CONTRACT/1" title="CONTRACT/1" icon="insert_link" />
      <mu-bottom-nav-item value="FILES/24" title="FILES/24" icon="folder_open" />
    </mu-bottom-nav>
  </mu-paper>
</template>

<script>
  export default {
    data() {
      return {
        bottomNav: 'ACCOUNT/53',
        bottomNavColor: 'ACCOUNT'
      }
    },
    methods: {
      handleChange(val) {
        this.bottomNav = val
      }
    }
  }
</script>

<style lang='less'>
  #navBar {
    margin-top: 2rem;
    .mu-bottom-nav-shift {
      font-family: SFProDisplay-Bold;
      background: rgba(40, 38, 50, 1);
    }
    .mu-bottom-item-text{
      color: rgba(122, 116, 153, 1);
    }
    .mu-bottom-item-icon{
      font-size: 0.7rem;
    }
  }
</style>
