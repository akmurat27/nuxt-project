<template>
    <div>        
        <header>
            <nav class="nav" :class="{'navbar_scrolled': isScrolled}">
                <div class="container">
                    <div class="nav-inner">
                        <nuxt-link to="/" class="nav-logo">
                            <img src="~/assets/nav-icons/Group48096276.png">
                        </nuxt-link>
                        <ul class="nav-links">
                            <li>
                                <nuxt-link class="nav-link" to="/" :class="{ 'active-nav-link': $route.path === '/' }">Baş sahypa</nuxt-link>
                            </li>
                            <div class="nav-btn">
                                <div class="lang">
                                    <div class="curr-lang">
                                        <nuxt-link to="/company" class="nav-link" :class="{ 'active-nav-link': $route.path === '/company' }">
                                            <span class="nav-link">Kompaniya</span>
                                        </nuxt-link>
                                    </div>
                                    <div class="lang-dropdown">
                                        <nuxt-link to="/company" :class="{ 'active-nav-link': $route.path === '/company' }">
                                            <span>Biz barada</span>
                                            <div class="comp-line"></div>
                                        </nuxt-link>
                                        <nuxt-link to="/hunarmenlermiz" :class="{ 'active-nav-link': $route.path === '/hunarmenlermiz' }">
                                            <span>Hunarmenlermiz</span>
                                            <div class="comp-line"></div>
                                        </nuxt-link>
                                        <nuxt-link to="/media" :class="{ 'active-nav-link': $route.path === '/media' }">
                                            <span>Media</span>
                                        </nuxt-link>
                                    </div>
                                </div>
                            </div>
                            <li>
                                <nuxt-link to="/hyzmatlar" class="nav-link" :class="{ 'active-nav-link': $route.path === '/hyzmatlar' }">
                                    <span class="nav-link">Hyzmatlar</span>
                                </nuxt-link>
                            </li>
                            <li>
                                <nuxt-link to="/tazelikler" class="nav-link" :class="{ 'active-nav-link': $route.path === '/tazelikler' }">
                                    <span class="nav-link">Täzelikler</span>
                                </nuxt-link>
                            </li>
                                <div class="nav-btn-drop">
                                    <div class="lang-drop-inner">
                                        <div class="curr-lang-drop">
                                            <nuxt-link class="nav-link" to="/logistika/railway" :class="{ 'active-nav-link': $route.path === '/logistika/railway' }">Logistika</nuxt-link>
                                            <img src="~/assets/nav-icons/Vector.png" alt="" />
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
                                    <a href="#" class="nav-link">EN</a>
                                    <img src="~/assets/nav-icons/Vector.png" alt="" />
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
                                        <li @click="selectItem('item1')">
                                            <span class="nav-a">
                                                <nuxt-link to="/" :class="{ 'active-nav-burger-li': $route.path === '/' }">Bas sahypa </nuxt-link>
                                            </span>
                                        </li>
                                        <li @click="selectItem('item2')">
                                            <span class="nav-a">
                                                <nuxt-link to="/company" :class="{ 'active-nav-burger-li': $route.path === '/company' }">Kompaniya</nuxt-link>
                                            </span>
                                        </li>
                                        <li @click="selectItem('item3')">
                                            <span class="nav-a">
                                                <nuxt-link to="/hyzmatlar" :class="{ 'active-nav-burger-li': $route.path === '/hyzmatlar' }"> Hyzmatlar </nuxt-link>
                                            </span>
                                        </li>
                                        <li @click="selectItem('item4')">
                                            <span class="nav-a">
                                                <nuxt-link to="/tazelikler"  :class="{ 'active-nav-burger-li': $route.path === '/tazelikler' }"> Tazelikler </nuxt-link>
                                            </span>
                                        </li>
                                        <li @click="selectItem('item5')">
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

                        <div class="nav-comp">
                            <a href="#" class="toggle-button"  @click="toggleNav">
                                <span class="bar" :class="{ 'active-bar': isActive }"></span>
                                <span class="bar" :class="{ 'active-bar': isActive }"></span>
                                <span class="bar" :class="{ 'active-bar': isActive }"></span>
                            </a>    
                        </div>
                    </div>
                </div>
            </nav>
        </header>
    </div>
</template>

<script>
export default{
    data(){
        return{
            isScrolled: false,
            isMenuOpen: false,
            isActive: false,
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
                this.isActive = true;
                document.body.style.overflow = 'visible';
            }
        },
    },
}
</script>
