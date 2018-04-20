<template>
  <mu-flexbox class="mt8" id="userInfo">
    <mu-flexbox-item order="1" span="200" class="flex-demo" grow='3'>
      <mu-list>
        <mu-list-item>
          <mu-avatar slot="left" src="http://www.muse-ui.org/images/uicon.jpg" />
          <p class="username">
            Martin-Chen
          </p>
          <p class="user-info">
            View and edit Digital ID
          </p>
        </mu-list-item>
      </mu-list>
    </mu-flexbox-item>
  </mu-flexbox>
</template>

<script>
  export default {}
</script>

<style lang='less'>
  #userInfo {
    color: #fff;
    .flex-demo {
      height: 2rem;
      width: 2rem;
    }
    .mu-item-wrapper {
      padding-left: 0.6rem;
      height: 2rem;
    }
    margin-top: 0.5rem;
    .mu-item-left {
      height: 2rem;
      width: 2rem;
      .mu-avatar {
        height: 100%;
        width: 100%;
      }
    }
    .mu-item.show-left {
      padding-left: 3rem;
      font-size: 0.8rem;
      font-family: SFProDisplay-Bold;
      color: rgba(255, 255, 255, 1);
      line-height: 0.96rem;
      p {
        margin: 0px;
      }
      .user-info {
        font-size: 0.37rem;
        font-family: SFProText-Regular;
        color: rgba(122, 116, 153, 1);
        line-height: 0.43rem;
      }
    }
  }
</style>
