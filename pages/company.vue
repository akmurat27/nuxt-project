<template>
    <div>
        <div class="about-company">
            <div class="company-page">
                <span>Kompaniýamyz hakynda</span>
                <div class="gradient"></div>
                <p>HJ "Hazar logistik" konteýner hyzmatyny, demir ýol gatnawyny ,awtoulag gatnawyny, deňiz gatnawyny, howa gatnawyny we multimodal gatnawyny, başgada esasanam howply harytlary daşamak bilen baglanyşykly transport we logistika hyzmatlarynyň doly toplumyny hödürlemekden hoşal. Gysga wagtyň içinde, hojalyk jemgyýetimiz köp tejribe toplady we import, eksport, üstaşyr amallary, şeýle hem Türkmenistanyň çäginden, GDA ýurtlarynyň üsti bilen daşamak üçin bütin dünýäde, hyzmatdaşlaryň we hyzmat üpjün edijileriň giň ulgamyny döretdi. Şunuň bilen baglylykda, Türkmenistanyň çäginden üstaşyr geçýän demir ýol gatnawy üçin ugradyş töleginiň 1% göterimdigini (transport mukdaryndan) habar bermek isleýäris. HJ "Hazar Logistik", Türkmenistanda ulag we logistika hyzmatlary pudagynda, iň ýokary orny eýelemäge we halkara arenasyna çykmaga çalyşýar. Müşderilerimiz, Türkmenistandaky işleriňiz bilen baglanyşykly soraglar ýa-da düşündirişler ýüze çykan halatynda ikirjiňlenmän biziň bilen habarlaşyp bilerler. Müşderilerimize iň oňat hünär çemeleşmesini we hünärmenlerimiziň iň ýokary ünsüni, şeýle hem bäsdeşlik bahalaryny hödürlemekden hoşal.</p>
            </div>
            <img src="~/assets/about-company/tm 1.png">
        </div>
        <div class="achieves">
            <div class="achieve">
                <span>Üstünlikler we sylaglar</span>
                <div class="gradient"></div>
            </div>
            <div class="achieve-images">
                <img src="~/assets/achieve/letter1 1.png" class="img">
                <img src="~/assets/achieve/letter1 1 (1).png" class="img disp-none">
                <img src="~/assets/achieve/Group 1000005764.png" class="img-1">
                <img src="~/assets/achieve/Group 1000005761.png" class="img-1">
            </div>
        </div>
        <div class="hyzmatdaslar">
            <div class="main-partner">
                <span>Biziň hyzmatdaşlarymyz</span>
            </div>
            <div class="swiper-container" ref="swiperContainer">
                <div class="swiper-wrapper">
                    <!-- Ручное добавление каждого слайда -->
                    <div class="swiper-slide">
                        <img src="~/assets/hyzmatdaslar/path2.png" alt="Logo 1" class="logo-image" />
                    </div>
                    <div class="swiper-slide">
                        <img src="~/assets/hyzmatdaslar/image 9.png" alt="Logo 2" class="logo-image" />
                    </div>
                    <div class="swiper-slide">
                        <img src="~/assets/hyzmatdaslar/Fortune.png" alt="Logo 3" class="logo-image" />
                    </div>
                    <div class="swiper-slide">
                        <img src="~/assets/hyzmatdaslar/Business web.png" alt="Logo 4" class="logo-image" />
                    </div>
                    <div class="swiper-slide">
                        <img src="~/assets/hyzmatdaslar/Mashable.png" alt="Logo 4" class="logo-image" />
                    </div>
                    <div class="swiper-slide">
                        <img src="~/assets/hyzmatdaslar/path2.png" alt="Logo 4" class="logo-image" />
                    </div>
                    <div class="swiper-slide">
                        <img src="~/assets/hyzmatdaslar/path2.png" alt="Logo 1" class="logo-image" />
                    </div>
                    <div class="swiper-slide">
                        <img src="~/assets/hyzmatdaslar/image 9.png" alt="Logo 2" class="logo-image" />
                    </div>
                    <div class="swiper-slide">
                        <img src="~/assets/hyzmatdaslar/Fortune.png" alt="Logo 3" class="logo-image" />
                    </div>
                </div>
            </div>
        </div>
        <div class="container">
            <div class="contact">
                <div class="number">
                    <div>
                        <span>Sowallaryňyz üçin bize ýüz tutuň!</span>
                        <p>Esteem spirit temper too say adieus who direct esteem. It look estee luckily or picture placing.</p>
                    </div>
                    <div>
                        <button>+99363 74 62 68</button>
                    </div>
                </div>
                <div class="form">
                    <div class="main-inputs">
                        <input autocomplete="off" name="name" id="name" type="text" placeholder="Your name" class="input-1">
                        <input autocomplete="off" name="password" id="password" type="text" placeholder="Your name" class="input-1">
                        <input autocomplete="off" name="email" id="email" type="email" placeholder="Email" class="input-1">
                        <input autocomplete="off" name="number" id="number" type="text" placeholder="Phone number" class="input-1">
                    </div>
                    <div class="main-input-2">
                        <input autocomplete="off" name="text-field" id="text-field" class="input-2" />
                    </div>
                    <button class="btn">Send Estimate</button>
                </div>
            </div>
        </div>
        <div class="map">
            <img src="~/assets/about-company/karta.png">
        </div>
    </div>
</template>

<script>
import Swiper from 'swiper';
import 'swiper/swiper-bundle.css';
export default {
    mounted() {
        this.initializeSwiper();
    },
    methods: {
        initializeSwiper() {
            new Swiper(this.$refs.swiperContainer, {
                spaceBetween: 20,
                loop: true,
                autoplay: {
                    delay: 3000,
                    disableOnInteraction: false,
                },
                breakpoints: {
                    // When window width is >= 640px
                    640: {
                        slidesPerView: 5,
                    },
                    // When window width is < 640px
                    0: {
                        slidesPerView: 2,
                    },
                },
            });
        },
    }
}
</script>
