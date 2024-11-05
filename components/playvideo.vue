<template>
    <div class="container">
        <section class="section-two">
            <div class="page-1">
                <span class="habar">BILELIKDE BIR ADIM ONDE</span>
                <div class="gradient"></div>
            </div>
            <div class="swiper-container swiper-two">
                <div class="swiper-wrapper">
                    <!-- Swiper Slide with Video -->
                    <div class="swiper-slide">
                        <div class="video-container">
                            <!-- Image with Play Button Overlay -->
                            <img 
                                src="~/assets/playvideo/448877118_752739253604984_1341900404665377833_n 1 (1).png" 
                                alt="Video Thumbnail" 
                                class="video-thumbnail" 
                            />
                            <div @click="playVideo" class="playbtn">
                                <img src="~/assets/playvideo/Group 1000005726.png">
                            </div>

                            <!-- Full-Screen Video Overlay -->
                            <div v-if="isPlaying" class="video-overlay">
                            <video controls autoplay class="video-player" ref="videoPlayer" src="~/assets/heropage/videoURL.mp4"></video>
                                <button @click="closeVideo" class="close-button">Close</button>
                            </div>
                        </div>
                    </div>

                    <div class="swiper-slide">
                        <div class="video-container">
                            <!-- Image with Play Button Overlay -->
                            <img 
                                src="~/assets/playvideo/448877118_752739253604984_1341900404665377833_n 1 (2).png" 
                                alt="Video Thumbnail" 
                                class="video-thumbnail" 
                            />
                            <div class="playbtn" @click="playVideo">
                                <img src="~/assets/playvideo/Group 1000005726.png">
                            </div>

                            <!-- Full-Screen Video Overlay -->
                            <div v-if="isPlaying" class="video-overlay">
                                <video controls autoplay class="video-player" ref="videoPlayer">
                                <source :src="videoUrl" type="video/mp4" />
                                Your browser does not support the video tag.
                                </video>
                                <button @click="closeVideo" class="close-button">Close</button>
                            </div>
                        </div>
                    </div>

                    <div class="swiper-slide">
                        <div class="video-container">
                        <!-- Image with Play Button Overlay -->
                        <img 
                            src="~/assets/playvideo/448877118_752739253604984_1341900404665377833_n 1 (3).png" 
                            alt="Video Thumbnail" 
                            class="video-thumbnail" 
                        />
                        <div class="playbtn" @click="playVideo">
                            <img src="~/assets/playvideo/Group 1000005726.png">
                        </div>

                        <!-- Full-Screen Video Overlay -->
                        <div v-if="isPlaying" class="video-overlay">
                            <video controls autoplay class="video-player" ref="videoPlayer">
                            <source :src="videoUrl" type="video/mp4" />
                            Your browser does not support the video tag.
                            </video>
                            <button @click="closeVideo" class="close-button">Close</button>
                        </div>
                        </div>
                    </div>

                    <div class="swiper-slide">
                        <div class="video-container">
                        <!-- Image with Play Button Overlay -->
                        <img 
                            src="~/assets/playvideo/448877118_752739253604984_1341900404665377833_n 1 (4).png" 
                            alt="Video Thumbnail" 
                            class="video-thumbnail" 
                        />
                        <div class="playbtn" @click="playVideo">
                            <img src="~/assets/playvideo/Group 1000005726.png">
                        </div>

                        <!-- Full-Screen Video Overlay -->
                        <div v-if="isPlaying" class="video-overlay">
                            <video controls autoplay class="video-player" ref="videoPlayer">
                            <source :src="videoUrl" type="video/mp4" />
                            Your browser does not support the video tag.
                            </video>
                            <button @click="closeVideo" class="close-button">Close</button>
                        </div>
                        </div>
                    </div>

                    <div class="swiper-slide">
                        <div class="video-container">
                        <!-- Image with Play Button Overlay -->
                        <img 
                            src="~/assets/playvideo/448877118_752739253604984_1341900404665377833_n 1 (4).png" 
                            alt="Video Thumbnail" 
                            class="video-thumbnail" 
                        />
                        <div class="playbtn" @click="playVideo">
                            <img src="~/assets/playvideo/Group 1000005726.png">
                        </div>

                        <!-- Full-Screen Video Overlay -->
                        <div v-if="isPlaying" class="video-overlay">
                            <video controls autoplay class="video-player" ref="videoPlayer">
                            <source :src="videoUrl" type="video/mp4" />
                            Your browser does not support the video tag.
                            </video>
                            <button @click="closeVideo" class="close-button">Close</button>
                        </div>
                        </div>
                    </div>

                    <div class="swiper-slide">
                        <div class="video-container">
                        <!-- Image with Play Button Overlay -->
                        <img 
                            src="~/assets/playvideo/448877118_752739253604984_1341900404665377833_n 1 (6).png" 
                            alt="Video Thumbnail" 
                            class="video-thumbnail" 
                        />
                        <div class="playbtn" @click="playVideo">
                            <img src="~/assets/playvideo/Group 1000005726.png">
                        </div>

                        <!-- Full-Screen Video Overlay -->
                        <div v-if="isPlaying" class="video-overlay">
                            <video controls autoplay class="video-player" ref="videoPlayer">
                            <source :src="videoUrl" type="video/mp4" />
                            Your browser does not support the video tag.
                            </video>
                            <button @click="closeVideo" class="close-button">Close</button>
                        </div>
                        </div>
                    </div>

                    <div class="swiper-slide">
                        <div class="video-container">
                        <!-- Image with Play Button Overlay -->
                        <img 
                            src="~/assets/playvideo/448877118_752739253604984_1341900404665377833_n 1 (1).png" 
                            alt="Video Thumbnail" 
                            class="video-thumbnail" 
                        />
                        <div class="playbtn" @click="playVideo">
                            <img src="~/assets/playvideo/Group 1000005726.png">
                        </div>

                        <!-- Full-Screen Video Overlay -->
                        <div v-if="isPlaying" class="video-overlay">
                            <video controls autoplay class="video-player" ref="videoPlayer">
                            <source :src="videoUrl" type="video/mp4" />
                            Your browser does not support the video tag.
                            </video>
                            <button @click="closeVideo" class="close-button">Close</button>
                        </div>
                        </div>
                    </div>

                    <div class="swiper-slide">
                        <div class="video-container">
                            <!-- Image with Play Button Overlay -->
                            <img 
                                src="~/assets/playvideo/448877118_752739253604984_1341900404665377833_n 1 (2).png" 
                                alt="Video Thumbnail" 
                                class="video-thumbnail" 
                            />
                            <div class="playbtn" @click="playVideo">
                                <img src="~/assets/playvideo/Group 1000005726.png">
                            </div>

                            <!-- Full-Screen Video Overlay -->
                            <div v-if="isPlaying" class="video-overlay">
                                <video controls autoplay class="video-player" ref="videoPlayer">
                                    <source :src="videoUrl" type="video/mp4" />
                                    Your browser does not support the video tag.
                                </video>
                                <button @click="closeVideo" class="close-button">Close</button>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="swiper-pagination swiper-pagination-two"></div>
            </div>
        </section>
    </div>
</template>

<script>
import { Swiper, Pagination } from 'swiper';
import 'swiper/swiper-bundle.css';
import videoUrl from "~/assets/heropage/videoURL.mp4";
Swiper.use([Pagination]);

export default {
    name: 'PlayVideo',
    data () {
        return {
            isPlaying: false,
            videoUrl
        }
    },
    components: {
        Swiper,
        Pagination,
        videoUrl
    },
    name: 'MySwiper',
    mounted() {
        const swiper = new Swiper('.swiper-two', {
            slidesPerView: 4,
            spaceBetween: 0,
            modules: [Pagination],
            pagination: {
                el: '.swiper-pagination-two',
                clickable: true,
                dynamicBullets: true,
            },
            loop: true,
            breakpoints: {
                // When window width is >= 640px
                640: {
                    slidesPerView: 4, // 3 slides per view for larger screens
                },
                // When window width is < 640px
                0: {
                    slidesPerView: 2, // 2 slides per view for small screens
                },
            },
        });
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
};
</script>

<style>
</style>