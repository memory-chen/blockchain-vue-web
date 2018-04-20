<template>
  <div class="demo-infinite-container">
    <mu-list>
      <div v-for="(item,index) in list" :key="index" class="item-list-box">
        <mu-list-item class="mt8">
          <mu-flexbox>
            <mu-flexbox-item class="flex-demo" grow='2'>
              <div class="demo-paper">
                oxFd
              </div>
            </mu-flexbox-item>
            <mu-flexbox-item class="flex-demo" grow='5'>
              <p class="account menu">
                <span><i class="mdui-icon material-icons">more_horiz</i></span>
              </p>
              <p class="account name">
                <b>MainAccount</b>
              </p>
              <p class="account money">
                <b>121,234,567,890.</b> <i>00</i>
              </p>
            </mu-flexbox-item>
          </mu-flexbox>
          <mu-flexbox class="hash-box">
            <mu-flexbox-item class="accunt hash" grow='3'>
              0xFD0fC3450bCB1E9585DE82A81372FD9dC1d52078
            </mu-flexbox-item>
            <mu-flexbox-item class="accunt hash" grow='1'>
            </mu-flexbox-item>
          </mu-flexbox>
        </mu-list-item>
        <mu-divider/>
      </div>
    </mu-list>
    <mu-float-button icon="add" secondary class="demo-float-button" />
    <mu-infinite-scroll :scroller="scroller" :loading="loading" @load="loadMore" />
  </div>
</template>

<script>
  export default {
    data() {
      const list = []
      for (let i = 0; i < 10; i++) {
        list.push('item' + (i + 1))
      }
      return {
        list,
        num: 10,
        loading: false,
        scroller: null
      }
    },
    mounted() {
      this.scroller = this.$el
    },
    methods: {
      loadMore() {
        this.loading = true
        setTimeout(() => {
          for (let i = this.num; i < this.num + 10; i++) {
            this.list.push('item' + (i + 1))
          }
          this.num += 10
          this.loading = false
        }, 2000)
      }
    },
    computed: {
      backgroundObject() {
        var rgba1 = Math.floor(Math.random() * 255) + ',' + Math.floor(Math.random() * 255) + ', ' + Math.floor(Math.random() * 255) + ', 1'
        var rgba2 = Math.floor(Math.random() * 255) + ',' + Math.floor(Math.random() * 255) + ', ' + Math.floor(Math.random() * 255) + ', 1'
        return {
          background: 'linear-gradient(90deg, rgba(' + rgba1 + '), rgba(' + rgba2 + '))'
        }
      }
    },
  }
</script>

<style scoped lang='less'>
  .demo-infinite-container {
    /* width: 256px; */
    height: 10.7rem;
    overflow: auto;
    -webkit-overflow-scrolling: touch; // border: 1px solid #d9d9d9;
    margin-top: 10px;
    .mt8 {
      // width: 9rem;
      height: 5rem;
      background: linear-gradient(90deg, rgba(89, 147, 255, 1), rgba(92, 66, 222, 1));
      border-radius: 0.43rem;
    }
    .item-list-box {
      padding: 10px 20px;
    }
    .account {
      color: #fff;
      margin: 0px;
      text-align: right;
      margin: 0.2rem 0px;
      min-height: .8rem;
    }
    .name {
      font-size: 0.48rem;
      font-family: SFProText-Bold;
      line-height: 0.56rem;
    }
    .money {
      font-size: 0.53rem;
      font-family: SFProDisplay-Bold;
      line-height: 0.64rem;
    }
    .demo-paper {
      display: inline-block;
      height: 1.3rem;
      width: 1.3rem;
      border: 2px solid #fff;
      border-radius: 50%;
      color: #fff;
      text-align: center;
      line-height: 1.3rem;
      font-size: 0.37rem;
    }
    .mu-flexbox-item.flex-demo {
      text-align: center;
    }
    .hash-box {
      border-top: 1px solid rgba(255, 255, 255, 0.8);
    }
    .mu-flexbox-item.accunt.hash {
      color: #fff;
      text-align: left;
      word-wrap: break-word;
    }
    .demo-float-button {
      position: fixed;
      bottom: 20px;
      left: 50%;
      transform: translateX(-50%); // background: #fff;
      // opacity: 0.65;
    }
    .mu-float-button-secondary {
      background-color: #fff9;
    }
  }
</style>
