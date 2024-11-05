<template>
    <div>
        <div class="container">
            <div class="header">
                <span class="main-title">Logistika</span>
                /
                <span class="main-title-2">Demir ýol ýük gatnawlary</span>
            </div>
            <div class="main-page">
                <div class="aside">
                    <div class="aside-header">
                        <span>Demir ýol ýük gatnawlary</span>
                    </div>
                    <ul class="list">
                        <li>
                            <nuxt-link to="/logistika/railway" exact-active-class="active-aside-link" class="nav-link">
                                <img src="~/assets/railway/Vector(1).svg">
                                Logistika
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/logistika/yerli" exact-active-class="active-aside-link" class="nav-link">
                                <img src="~/assets/railway/Icon (2).svg">
                                Baha hasaplamak
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/logistika/demir-yol" exact-active-class="active-aside-link">
                                <img :src="demirYolIcon">
                                Demir ýol menzilleri
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/logistika/wagonlar" exact-active-class="active-aside-link" class="nav-link">
                                <img src="~/assets/railway/Icon (4).svg">
                                Wagonlar
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/logistika/harytlar" exact-active-class="active-aside-link" class="nav-link">
                                <img src="~/assets/railway/Icon (5).svg">
                                Harytlaryň kodlary
                            </nuxt-link>
                        </li>
                    </ul>
                </div>
                <div class="logistika">
                    <span>MENZILLER:</span>
                    <p>Bitewi çyzgyt boýunça menziller</p>
                    <div class="image-options">
                        <div>
                            <img src="~/assets/railway/image 13.png">
                        </div>
                        <div class="options">
                            <select name="search" id="search">
                                <option value="1">Gözleg..</option>
                                <option value="2">2</option>
                                <option value="3">3</option>
                            </select>
                            <select name="options" id="options">
                                <option value="1">Stansiyan ady yada kody</option>
                                <option value="2">2</option>
                                <option value="3">3</option>
                            </select>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Icon3 from '~/assets/railway/Icon (3).svg';
import ActiveIcon3 from '~/assets/railway/Icon (11).svg';
export default {
    computed: {
        demirYolIcon() {
            return this.$route.path === '/logistika/demir-yol' ? ActiveIcon3 : Icon3;
        },
    }
}
</script>

<style lang="scss" scoped>
.container{
    width: 100%;
    max-width: 1420px;
    margin: 0 auto;
}
.header{
    margin-top: 120px;
    .main-title{
        color: #14509D;
        font-size: 16px;
        font-weight: 600;
    }
    .main-title-2{
        color: #3A4052BF;
        font-size: 16px;
        font-weight: 600;
    }
}
.main-page{
    margin-top: 50px;
    display: flex;
    margin-bottom: 130px;
    .aside{
        border-right: 1px solid #C4C4C4;
        width: 295px;
        height: auto;
        .aside-header{
            font-size: 18px;
            font-weight: 800;
            color: #14509D;
        }
        .list{
            width: 295px;
            height: 291px;
            margin-top: 20px;
            display: flex;
            flex-direction: column;
            gap: 15px;
            li{
                list-style: none;
                width: 273px;
                height: 43px;
                display: flex;
                align-items: center;
                gap: 10px;
            }
            img{
                margin-right: 10px
            }
            .active-aside-link{
                background-color: #14509D; /* Example styling for active link */
                border: none;
                color: white;
                font-size: 18px;
                font-weight: 600;
                width: 273px;
                height: 43px;
                border-radius: 6px;
                text-decoration: none;
                display: flex;
                align-items: center;
                padding-left: 25px; 
            }
            .nav-link{
                color: black;
                font-size: 18px;
                font-weight: 600;
                width: 273px;
                height: 43px;
                border-radius: 6px;
                text-decoration: none;
                display: flex;
                align-items: center;
                padding-left: 25px; 
            }
        }
    }
    .logistika{
        margin-left: 30px;
        span{
            font-size: 32px;
            font-weight: 800;
            color:#3A4052;
        }
        p{
            font-size: 18px;
            font-weight: 400;
            color:#3A4052;
            margin: 15px 0px;
        }
        .image-options{
            display: flex;
            gap: 40px;
            .options{
                display: flex;
                flex-direction: column;
                gap: 21px;
                select{
                    width: 359px;
                    height: 48px;
                    padding: 15px 30px;
                    border: 1px solid #B3B3B3;
                    border-radius: 6px;
                    appearance: none;
                    -webkit-appearance: none;
                    -moz-appearance: none;
                    background: url('~/assets/railway/Vector.svg') no-repeat right 20px center;
                }
            }
        }
    }
}
</style>