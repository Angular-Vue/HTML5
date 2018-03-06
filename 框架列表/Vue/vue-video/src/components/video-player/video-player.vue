<!-- 组件功能：本项目中的视频播放组件 -->
<!-- 如视频需实现自动播放功能，视频应默认存在页面中，不可使用v-if-->
<template>
  <div id="video-player">
    <player ref="player"
            class="player"
            :options="playerOptions"
            @play="onPlayerPlay($event)"
            @pause="onPlayerPause($event)"
            @ended="onPlayerEnded($event)">
    </player>
  </div>
</template>

<script type="text/ecmascript-6">
  import player from './base/player.vue'
  export default {
    name: 'video-player',
    components:{player},
    props: {
      video: {
        type: Object,
        default(){
          return{video_url:'',video_image:''}
        }
      }
    },
    data(){
      return {
        playerOptions: {//video参数
          autoplay: false,
          bigPlayButton: false,
          controlBar: {
            playToggle: {},
            currentTimeDisplay: true,
            timeDivider: true,
            durationDisplay: true,
            remainingTimeDisplay: false,
            progressControl: {},
            volumeMenuButton: false,
            fullscreenToggle: false
          },
          sources: [{
            type: "video/mp4",
            src: this.video.video_url
          }],
          poster: this.video.video_image,
        }
      }
    },
    computed: {
      player() {
        return this.$refs.player.player;
      }
    },
    methods: {
      // listen event
      onPlayerPlay(player){
        this.$emit('play');
      },
      onPlayerPause(player){
        this.$emit('pause');
      },
      onPlayerEnded(player){
        this.$emit('end');
      },
      //从头播放（自动播放功能须由按钮点击触发）
      restart_play(){
        this.player.currentTime(0);
        this.player.play();
      },
      //停止播放
      stop_play(){
        this.player.currentTime(0);
        this.player.pause();
      },
    }
  };
</script>

<style rel="stylesheet/scss" lang="scss">
  @function pxToRem($px) {
    @return $px;
  }
  #video-player {
    .player{
      .video-js.vjs-custom-skin {
      }
      .vjs-control-bar{
        .vjs-play-control { //播放暂停按钮
          &.vjs-playing {
            /*background: url("~ASSETS/images/components/video-player/ic_pause.webp") no-repeat center;*/
          }
          &.vjs-paused {
            /*background: url("~ASSETS/images/components/video-player/ic_play.webp") no-repeat center;*/
          }
          &:before {
            content: '';
          }
        }
        .vjs-progress-control { //进度条
          .vjs-progress-holder { //进度容器
            .vjs-load-progress { //加载进度
            }
            .vjs-play-progress { //当前进度
              &:before { //进度条小红点
              }
            }
            .vjs-mouse-display { //鼠标所在的数字
              display: none;
            }
          }
        }
        .vjs-time-control { //时间
          .vjs-control-text{
          }
        }
      }
      .vjs-has-started.vjs-user-inactive.vjs-playing .vjs-control-bar {
        /*visibility: visible;//取消自动隐藏功能*/
      }
    }
  }
</style>
