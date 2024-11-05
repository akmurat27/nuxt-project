<template>
    <div>        
        <header>
            <nav class="nav" :class="{'navbar_scrolled': isScrolled}">
                <div class="container">
                    <div class="nav-inner">
                        <nuxt-link to="/" class="nav-logo">
                            <img :src="isScrolled ? logoScrolled : logoDefault">
                        </nuxt-link>
                        <ul class="nav-links">
                            <li>
                                <nuxt-link class="nav-link" to="/">
                                    <span class="main-line">Baş sahypa</span>
                                </nuxt-link>
                            </li>
                            
                            <div class="nav-btn">
                                <div class="lang">
                                    <div class="curr-lang">
                                        <nuxt-link to="/company" class="nav-link">Kompaniýa</nuxt-link>
                                    </div>
                                    <div class="lang-dropdown">
                                        <nuxt-link to="/company">
                                            <span>Biz barada</span>
                                            <div class="comp-line"></div>
                                        </nuxt-link>
                                        <nuxt-link to="/hunarmenlermiz">
                                            <span>Hunarmenlermiz</span>
                                            <div class="comp-line"></div>
                                        </nuxt-link>
                                        <nuxt-link to="/media">
                                            <span>Media</span>
                                        </nuxt-link>
                                    </div>
                                </div>
                            </div>
                            
                            <li>
                                <nuxt-link to="/hyzmatlar" class="nav-link">
                                    <span class="nav-link">Hyzmatlar</span>
                                </nuxt-link>
                            </li>
                            <li>
                                <nuxt-link to="/tazelikler" class="nav-link">
                                    <span class="nav-link">Täzelikler</span>
                                </nuxt-link>
                            </li>
                            <div class="nav-btn-drop">
                                <div class="lang-drop-inner">
                                    <div class="curr-lang-drop">
                                        <nuxt-link class="nav-link" to="/logistika/railway">Logistika</nuxt-link>
                                        <img :src="isScrolled ? iconScrolled : iconDefault" alt="" />
                                    </div>
                                    <div class="lang-drop">
                                        <nuxt-link to="/logistika/railway">Demir ýol gatnawy</nuxt-link>
                                        <div class="comp-line"></div>
                                        <nuxt-link to="/logistika/deniz/deniz-gatnawy">Deňiz gatnawy</nuxt-link>
                                    </div>
                                </div>
                            </div>
                        </ul>
                        <div class="nav-btn">
                            <div class="lang">
                                <div class="curr-lang">
                                    <a class="nav-link" href="#">EN</a>
                                    <img :src="isScrolled ? iconScrolled : iconDefault" alt="" />
                                </div>
                                <div class="lang-dropdown">
                                    <a href="#">RU</a>
                                    <div class="line"></div>
                                    <a href="#">TM</a>
                                </div>
                            </div>
                        </div>

                        <div class="nav-burger"  :class="{ active: isActive }" @click="handleNavClick">
                            <div class="nav-burger-wrapper">
                                <div class="nav-burger-logo-li">
                                    <div class="nav-burger-wrapper-logo">
                                        <img src="~/assets/nav-icons/Group48096276.png" alt="" />
                                    </div>
                                    <ul>
                                        <li  @click="selectItem('item1')">
                                            <span class="nav-a">
                                                <nuxt-link to="/">Bas sahypa </nuxt-link>
                                            </span>
                                        </li>
                                        <li  @click="selectItem('item2')">
                                            <span class="nav-a">
                                                <nuxt-link to="/company">Kompaniya</nuxt-link>
                                            </span>
                                        </li>
                                        <li  @click="selectItem('item3')">
                                            <span class="nav-a">
                                                <nuxt-link to="/hyzmatlar"> Hyzmatlar </nuxt-link>
                                            </span>
                                        </li>
                                        <li  @click="selectItem('item4')">
                                            <span class="nav-a">
                                                <nuxt-link to="/tazelikler"> Tazelikler </nuxt-link>
                                            </span>
                                        </li>
                                        <li   @click="selectItem('item5')">
                                            <a class="nav-a">Logistika</a>
                                        </li>
                                    </ul>
                                </div>
                                <div class="nav-burger-wrapper-lang">
                                    <a class="mobile-curr-lang active-mobile-curr-lang" href="#">en</a>
                                    <a class="mobile-curr-lang" href="#">ru</a>
                                    <a class="mobile-curr-lang" href="#">tm</a>
                                </div>
                            </div>
                        </div>
                        <a href="#" class="toggle-button"  @click="toggleNav">
                            <span class="bar" :class="{ 'active-bar': isActive }"></span>
                            <span class="bar" :class="{ 'active-bar': isActive }"></span>
                            <span class="bar" :class="{ 'active-bar': isActive }"></span>
                        </a>    
                    </div>
                </div>
            </nav>
        </header>
    </div>
</template>

<script>
import logoDefault from '~/assets/nav-icons/Group1000005676.png';
import logoScrolled from '~/assets/nav-icons/Group48096276.png';
import iconDefault from '~/assets/nav-icons/Polygon 1.svg';
import iconScrolled from '~/assets/nav-icons/Vector.png';
export default{
    data(){
        return{
            isActive: false,
            isScrolled: false,
            logoDefault,
            logoScrolled,
            iconDefault,
            iconScrolled,
            isMenuOpen: false,
        };
    },
    mounted() {
        window.addEventListener('scroll', this.handleScroll);
    },
    beforeDestroy() {
        window.removeEventListener('scroll', this.handleScroll);
    },
    methods: {
        selectItem(item) {
            console.log(`Selected: ${item}`);
            this.isMenuOpen = false; // Close the menu
        },
        handleScroll() {
            this.isScrolled = window.scrollY > 100; // Change threshold as needed
        },
        toggleNav() {
            this.isActive = !this.isActive;
            document.body.style.overflow = this.isActive ? 'hidden' : 'visible';
        },
        handleNavClick(e) {
            if (e.target === this.$refs.navUl) {
                this.isActive = false;
                document.body.style.overflow = 'visible';
            }
        },
    },
}
</script>

<style>
</style>