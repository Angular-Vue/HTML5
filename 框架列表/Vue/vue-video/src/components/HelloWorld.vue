<template>
  <div class="hello">
    <video-player class="video-player"
                  ref="videoPlayer"
                  :class="{'all-hide':false}"
                  :video="video"
                  @end="end_play"></video-player>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      video: {
        video_url:'http://babylife.qiniudn.com/FtRVyPQHHocjVYjeJSrcwDkApTLQ',video_image:'http://static.fdc.com.cn/avatar/usercenter/5996999fa093c04d4b4dbaf1_162.jpg'
      }
    }
  },
  methods: {
    end_play(){
      console.info("结束")
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
