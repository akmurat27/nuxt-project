<template>
    <div class="container">
      <div class="media-header">
        <div class="media-text">MEDIA</div>
        <div class="gradient"></div>
      </div>
      <div class="media-container">
          <div class="video-container">
            <img 
              src="~/assets/playvideo/448877118_752739253604984_1341900404665377833_n 1 (1).png" 
              class="video-thumbnail"
              alt="Video Thumbnail" 
              @click="playVideo"
            >
            <div class="play">
              <img src="~/assets/heropage/Group 1000005726.svg" class="playbtn" @click="playVideo">
            </div>

            <!-- Video Player -->
            <div v-if="isPlaying" class="video-overlay">
                <video controls autoplay class="video-player">
                    <source :src="videoUrl" type="video/mp4" />
                    Your browser does not support the video tag.
                </video>
                <button @click="closeVideo" class="close-button">Close</button>
            </div>
          </div>
          <div class="video-container">
            <img 
              src="~/assets/playvideo/448877118_752739253604984_1341900404665377833_n 1 (2).png" 
              class="video-thumbnail"
              alt="Video Thumbnail" 
              @click="playVideo"
            >
            <div class="play">
              <img src="~/assets/heropage/Group 1000005726.svg" class="playbtn" @click="playVideo">
            </div>

            <!-- Video Player -->
            <div v-if="isPlaying" class="video-overlay">
                <video controls autoplay class="video-player">
                    <source :src="videoUrl" type="video/mp4" />
                    Your browser does not support the video tag.
                </video>
                <button @click="closeVideo" class="close-button">Close</button>
            </div>
          </div>
          <div class="video-container">
            <img 
              src="~/assets/playvideo/448877118_752739253604984_1341900404665377833_n 1 (3).png" 
              class="video-thumbnail"
              alt="Video Thumbnail" 
              @click="playVideo"
            >
            <div class="play">
              <img src="~/assets/heropage/Group 1000005726.svg" class="playbtn" @click="playVideo">
            </div>

            <!-- Video Player -->
            <div v-if="isPlaying" class="video-overlay">
                <video controls autoplay class="video-player">
                    <source :src="videoUrl" type="video/mp4" />
                    Your browser does not support the video tag.
                </video>
                <button @click="closeVideo" class="close-button">Close</button>
            </div>
          </div>
          <div class="video-container">
            <img 
              src="~/assets/playvideo/448877118_752739253604984_1341900404665377833_n 1 (4).png" 
              class="video-thumbnail"
              alt="Video Thumbnail" 
              @click="playVideo"
            >
            <div class="play">
              <img src="~/assets/heropage/Group 1000005726.svg" class="playbtn" @click="playVideo">
            </div>

            <!-- Video Player -->
            <div v-if="isPlaying" class="video-overlay">
                <video controls autoplay class="video-player">
                    <source :src="videoUrl" type="video/mp4" />
                    Your browser does not support the video tag.
                </video>
                <button @click="closeVideo" class="close-button">Close</button>
            </div>
          </div>
          <div class="video-container">
            <img 
              src="~/assets/playvideo/448877118_752739253604984_1341900404665377833_n 1 (1).png" 
              class="video-thumbnail"
              alt="Video Thumbnail" 
              @click="playVideo"
            >
            <div class="play">
              <img src="~/assets/heropage/Group 1000005726.svg" class="playbtn" @click="playVideo">
            </div>

            <!-- Video Player -->
            <div v-if="isPlaying" class="video-overlay">
                <video controls autoplay class="video-player">
                    <source :src="videoUrl" type="video/mp4" />
                    Your browser does not support the video tag.
                </video>
                <button @click="closeVideo" class="close-button">Close</button>
            </div>
          </div>
          <div class="video-container">
            <img 
              src="~/assets/playvideo/448877118_752739253604984_1341900404665377833_n 1 (2).png" 
              class="video-thumbnail"
              alt="Video Thumbnail" 
              @click="playVideo"
            >
            <div class="play">
              <img src="~/assets/heropage/Group 1000005726.svg" class="playbtn" @click="playVideo">
            </div>

            <!-- Video Player -->
            <div v-if="isPlaying" class="video-overlay">
                <video controls autoplay class="video-player">
                    <source :src="videoUrl" type="video/mp4" />
                    Your browser does not support the video tag.
                </video>
                <button @click="closeVideo" class="close-button">Close</button>
            </div>
          </div>
          <div class="video-container">
            <img 
              src="~/assets/playvideo/448877118_752739253604984_1341900404665377833_n 1 (3).png" 
              class="video-thumbnail"
              alt="Video Thumbnail" 
              @click="playVideo"
            >
            <div class="play">
              <img src="~/assets/heropage/Group 1000005726.svg" class="playbtn" @click="playVideo">
            </div>

            <!-- Video Player -->
            <div v-if="isPlaying" class="video-overlay">
                <video controls autoplay class="video-player">
                    <source :src="videoUrl" type="video/mp4" />
                    Your browser does not support the video tag.
                </video>
                <button @click="closeVideo" class="close-button">Close</button>
            </div>
          </div>
          <div class="video-container">
            <img 
              src="~/assets/playvideo/448877118_752739253604984_1341900404665377833_n 1 (4).png" 
              class="video-thumbnail"
              alt="Video Thumbnail" 
              @click="playVideo"
            >
            <div class="play">
              <img src="~/assets/heropage/Group 1000005726.svg" class="playbtn" @click="playVideo">
            </div>

            <!-- Video Player -->
            <div v-if="isPlaying" class="video-overlay">
                <video controls autoplay class="video-player">
                    <source :src="videoUrl" type="video/mp4" />
                    Your browser does not support the video tag.
                </video>
                <button @click="closeVideo" class="close-button">Close</button>
            </div>
          </div>
          <div class="video-container">
            <img 
              src="~/assets/playvideo/448877118_752739253604984_1341900404665377833_n 1 (1).png" 
              class="video-thumbnail"
              alt="Video Thumbnail" 
              @click="playVideo"
            >
            <div class="play">
              <img src="~/assets/heropage/Group 1000005726.svg" class="playbtn" @click="playVideo">
            </div>

            <!-- Video Player -->
            <div v-if="isPlaying" class="video-overlay">
                <video controls autoplay class="video-player">
                    <source :src="videoUrl" type="video/mp4" />
                    Your browser does not support the video tag.
                </video>
                <button @click="closeVideo" class="close-button">Close</button>
            </div>
          </div>
          <div class="video-container">
            <img 
              src="~/assets/playvideo/448877118_752739253604984_1341900404665377833_n 1 (2).png" 
              class="video-thumbnail"
              alt="Video Thumbnail" 
              @click="playVideo"
            >
            <div class="play">
              <img src="~/assets/heropage/Group 1000005726.svg" class="playbtn" @click="playVideo">
            </div>

            <!-- Video Player -->
            <div v-if="isPlaying" class="video-overlay">
                <video controls autoplay class="video-player">
                    <source :src="videoUrl" type="video/mp4" />
                    Your browser does not support the video tag.
                </video>
                <button @click="closeVideo" class="close-button">Close</button>
            </div>
          </div>
          <div class="video-container">
            <img 
              src="~/assets/playvideo/448877118_752739253604984_1341900404665377833_n 1 (3).png" 
              class="video-thumbnail"
              alt="Video Thumbnail" 
              @click="playVideo"
            >
            <div class="play">
              <img src="~/assets/heropage/Group 1000005726.svg" class="playbtn" @click="playVideo">
            </div>

            <!-- Video Player -->
            <div v-if="isPlaying" class="video-overlay">
                <video controls autoplay class="video-player">
                    <source :src="videoUrl" type="video/mp4" />
                    Your browser does not support the video tag.
                </video>
                <button @click="closeVideo" class="close-button">Close</button>
            </div>
          </div>
          <div class="video-container">
            <img 
              src="~/assets/playvideo/448877118_752739253604984_1341900404665377833_n 1 (4).png" 
              class="video-thumbnail"
              alt="Video Thumbnail" 
              @click="playVideo"
            >
            <div class="play">
              <img src="~/assets/heropage/Group 1000005726.svg" class="playbtn" @click="playVideo">
            </div>

            <!-- Video Player -->
            <div v-if="isPlaying" class="video-overlay">
                <video controls autoplay class="video-player">
                    <source :src="videoUrl" type="video/mp4" />
                    Your browser does not support the video tag.
                </video>
                <button @click="closeVideo" class="close-button">Close</button>
            </div>
          </div>
      </div>
    </div>
</template>

<script>
import videoUrl from "~/assets/heropage/videoURL.mp4";
export default{
  data() {
    return {
      isPlaying: false,
      videoUrl
    };
  },
  methods: {
    playVideo() {
      this.isPlaying = true;
      // Pause the video when the slide changes
      this.$refs.videoPlayer.play();
    },
    closeVideo() {
      this.isPlaying = false;
      this.$refs.videoPlayer.pause();
    },
  }
}
</script>

<style scoped>
.my_image_class {
  max-width: 100%;
  height: auto;
}
</style>