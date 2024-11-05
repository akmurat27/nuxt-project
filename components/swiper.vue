<template>
  <div>
    <section class="section-one">
      <div class="swiper-container swiper-one">
        <div class="swiper-wrapper">
          <!-- Slide 1 -->
          <div class="swiper-slide">
            <div class="main-title">
              <div class="animated-text image-text">
                <span v-for="(char, index) in currentText" :key="index" class="text-char">{{ char }}</span>
              </div>
              <nuxt-link to="#contact" class="text-decor">
                <button class="btn">
                  <span>Ýüz tutmak</span>
                  <img src="~/assets/nav-icons/ArrowRight.png" class="arrow" />
                </button>
              </nuxt-link>
            </div>
            <img src="~/assets/nav-icons/banner 5 1.png" alt="Dynamic Image" />
          </div>

          <!-- Slide 2 -->
          <div class="swiper-slide">
            <div class="main-title">
              <h1 ref="word" class="image-text"></h1>
              <nuxt-link to="#contact" class="text-decor">
                <button class="btn">
                  <span>Ýüz tutmak</span>
                  <img src="~/assets/nav-icons/ArrowRight.png" class="arrow" />
                </button>
              </nuxt-link>
            </div>
            <img src="~/assets/nav-icons/banner 4 1.png" alt="Dynamic Image" />
          </div>

          <!-- Slide 3 -->
          <div class="swiper-slide">
            <div class="main-title">
              <h1 ref="word" class="image-text"></h1>
              <nuxt-link to="#contact" class="text-decor">
                <button class="btn">
                  <span>Ýüz tutmak</span>
                  <img src="~/assets/nav-icons/ArrowRight.png" class="arrow" />
                </button>
              </nuxt-link>
            </div>
            <img src="~/assets/nav-icons/banner 2.png" alt="Dynamic Image" />
          </div>

          <!-- Slide 4 -->
          <div class="swiper-slide">
            <div class="main-title">
              <h1 ref="word" class="image-text"></h1>
              <nuxt-link to="#contact" class="text-decor">
                <button class="btn">
                  <span>Ýüz tutmak</span>
                  <img src="~/assets/nav-icons/ArrowRight.png" class="arrow" />
                </button>
              </nuxt-link>
            </div>
            <img src="~/assets/nav-icons/banner 3 (1).png" alt="Dynamic Image" />
          </div>

          <!-- Slide 5 -->
          <div class="swiper-slide">
            <div class="main-title">
              <h1 ref="word" class="image-text"></h1>
              <nuxt-link to="#contact" class="text-decor">
                <button class="btn">
                  <span>Ýüz tutmak</span>
                  <img src="~/assets/nav-icons/ArrowRight.png" class="arrow" />
                </button>
              </nuxt-link>
            </div>
            <img src="~/assets/homepage/5.png" alt="Dynamic Image" />
            <div class="linear-gradient"></div>
          </div>

          <!-- Slide 6 -->
          <div class="swiper-slide">
            <div class="main-title">
              <h1 ref="word" class="image-text"></h1>
              <nuxt-link to="#contact" class="text-decor">
                <button class="btn">
                  <span>Ýüz tutmak</span>
                  <img src="~/assets/nav-icons/ArrowRight.png" class="arrow" />
                </button>
              </nuxt-link>
            </div>
            <img src="~/assets/homepage/6.png" alt="Dynamic Image" />
            <div class="linear-gradient"></div>
          </div>

          <!-- Slide 7 -->
          <div class="swiper-slide">
            <div class="main-title">
              <h1 ref="word" class="image-text"></h1>
              <nuxt-link to="#contact" class="text-decor">
                <button class="btn">
                  <span>Ýüz tutmak</span>
                  <img src="~/assets/nav-icons/ArrowRight.png" class="arrow" />
                </button>
              </nuxt-link>
            </div>
            <img src="~/assets/homepage/7.png" alt="Dynamic Image" />
            <div class="linear-gradient"></div>
          </div>
        </div>

        <div class="swiper-pagination swiper-pagination-one"></div>
      </div>
    </section>
  </div>
</template>


  
<script>
import { Swiper, Pagination, Autoplay  } from 'swiper';
import 'swiper/swiper-bundle.css';

Swiper.use([Pagination, Autoplay ]);

export default {
  data () {
    return {
      texts: [
        'Hemişe öz wagtynda',
        // 'Второй текст',
        // 'Третий текст',
        // 'Четвертый текст',
      ],
      currentText: '',
      currentTextIndex: 0,
      animationDelay: 150, // Задержка между буквами
      isAnimating: false, // Флаг для анимации
    };
  },
  components: {
    Swiper,
    Pagination,
  },
  name: 'MySwiper',
  mounted() {
    this.startAnimation(); // Запускаем анимацию при монтировании компонента
    const swiper = new Swiper('.swiper-one', {
      autoplay: {
        delay: 3000,
      },
      modules: [Pagination],
      pagination: {
        el: '.swiper-pagination-one',
        clickable: true,
        dynamicBullets: true,
      },
      loop: true,
    });
  },
  beforeDestroy() {
    clearInterval(this.interval);  // Очищаем интервал, когда компонент уничтожается
  },
  methods: {
    startAnimation() {
      this.animateText(this.texts[this.currentTextIndex]);
    },
    animateText(text) {
      this.currentText = ''; // Сбросить текущее значение текста
      const chars = text.split(''); // Разбить текст на символы

      // Появление символов по очереди
      chars.forEach((char, index) => {
        setTimeout(() => {
          this.currentText += char; // Добавить символ к текущему тексту
          // Если последний символ добавлен, запускаем исчезновение
          if (index === chars.length - 1) {
            setTimeout(() => this.fadeOutText(chars.length), 1000); // Ждем 1 секунду перед исчезновением
          }
        }, index * this.animationDelay);
      });
    },
    fadeOutText(length) {
      const chars = this.currentText.split('');
      let fadeIndex = 0;

      const fadeOutInterval = setInterval(() => {
        if (fadeIndex < length) {
          chars[fadeIndex] = ''; // Удалить символ
          this.currentText = chars.join('');
          fadeIndex++;
        } else {
          clearInterval(fadeOutInterval); // Остановить интервал, когда все символы пропадут
          this.currentTextIndex = (this.currentTextIndex + 1) % this.texts.length; // Переключение на следующий текст
          this.startAnimation(); // Запускаем анимацию для нового текста
        }
      }, this.animationDelay);
    },
  },
};
</script>

  
<style scoped>
.animated-text {
  margin-top: 20px;
  font-size: 24px;
  font-weight: bold;
}

.text-char {
  display: inline-block;
  opacity: 0; /* Скрываем текст по умолчанию */
  transition: opacity 0.3s ease; /* Плавный переход */
}

.text-char:nth-child(n+1) {
  opacity: 1; /* По умолчанию показываем первый символ */
}
</style>
  