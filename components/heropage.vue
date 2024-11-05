<template>
    <section class="container">
        <div class="heropage">
            <div class="first-page">
                <div class="fontmain">Name üçin bizi saýlamaly?!</div>
                <div class="gradient"></div>
                <div class="text-section">
                    <h3 style="margin-bottom: 15px;">Çünki biz geljekki ösüşiňiziň kepili</h3>
                    <p>Hojalyk jemgyýetimiziň demir ýol, deňiz, howa we awtoulag ýük gatnawlaryny öz wagtynda, ýokary derejede amala aşyrmak üçin döwrebap çözgütleri bar. Siz gämi, otly, uçar ýa-da awtoulag bilen ýük gatnawlaryny amala aşyrmak isleýärsiňizmi?! Import, eksport ýa-da üstaşyr ýük gatnawlaryny amala aşyrmakçymy?! Onda size «Hazar logistik» hojalyk jemgyýetiniň hyzmatlary juda zerur</p> 
                </div>
                <button class="btn">DOLY MAGLUMAT</button>
            </div>
            <div class="half-page">
                <div class="big-pic"></div>
                <div class="video-container">
                  <img :src="img" class="image video-thumbnail"
                      alt="Video Thumbnail" 
                      @click="playVideo"
                  >
                  <div class="play">
                      <img :src="icon" @click="playVideo">
                  </div>

                  <!-- Video Player -->
                  <div v-if="isPlaying" class="video-overlay">
                    <video controls autoplay class="video-player">
                      <source :src="video" type="video/mp4" />
                      Your browser does not support the video tag.
                    </video>
                    <button @click="closeVideo" class="close-button">Close</button>
                  </div>
                </div>
                <button class="btn-1">DOLY MAGLUMAT</button>
            </div>
        </div>
    </section>
</template>

<script>
import img from "~/assets/heropage/448877118_752739253604984_1341900404665377833_n 1.png"
import icon from "~/assets/heropage/Group 1000005726.svg"
import video from "~/assets/heropage/videoURL.mp4"
export default {
  data() {
    return {
      isPlaying: false,
      img,
      icon,
      video,  // Replace with your video URL
    };
  },
  methods: {
    playVideo() {
      this.isPlaying = true;
    },
    closeVideo() {
      this.isPlaying = false;
    }
  }
};
</script>

<style lang="scss" scoped>


</style>
