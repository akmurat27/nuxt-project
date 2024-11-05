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
                            <nuxt-link to="/logistika/yerli" exact-active-class="active-aside-link">
                                <img :src="bahaHasaplamakIcon">
                                Baha hasaplamak
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/logistika/demir-yol" exact-active-class="active-aside-link" class="nav-link">
                                <img src="~/assets/railway/Icon (3).svg">
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
                    <div v-if="selectedPage === 'tabs'">
                        <ul class="tabs">
                            <li @click="activeTab = 'tab1'" :class="{ active: activeTab === 'tab1' }">
                                Ýerli
                            </li>
                            <li @click="activeTab = 'tab2'" :class="{ active: activeTab === 'tab2' }">
                                Import
                            </li>
                            <li @click="activeTab = 'tab3'" :class="{ active: activeTab === 'tab3' }">
                                Eksport
                            </li>
                            <li @click="activeTab = 'tab4'" :class="{ active: activeTab === 'tab4' }">
                                Üstaşyr
                            </li>
                        </ul>

                        <!-- Tab Content -->
                        <div v-if="activeTab === 'tab1'">
                            <div class="text-title">
                                <span>ÝÜK GATNAWLARY ÜÇIN BAHA HASAPLAMAK</span>
                                <div class="text-option">
                                    <p>Ýük gatnawlary boýunça baha hasaplamak isleseňiz aşakdakylary doldurmak arkaly amala aşyryp bilersiňiz</p>
                                    <div class="options">
                                        <select name="options" id="options" class="select-1" autocomplete="off">
                                            <option value="1">TMT</option>
                                            <option value="2">$</option>
                                            <option value="3">TL</option>
                                        </select>
                                        <select name="choose" id="choose" autocomplete="off">
                                            <option value="1">Hojalyk jemgyyeti</option>
                                            <option value="2">$</option>
                                            <option value="3">TL</option>
                                        </select>
                                    </div>
                                </div>
                            </div>
                            <div class="two-options">
                                <div class="options-elements">
                                    <span>UGRAÝAN ÝURDY:</span>
                                    <select name="country" id="country" autocomplete="off">
                                        <option value="1">Stansiýanyň adyny ýa-da koduny giriziň:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                                <div class="options-elements">
                                    <span>GIRIŞ NOKADY:</span>
                                    <select name="login" id="login" autocomplete="off">
                                        <option value="1">Stansiýanyň adyny ýa-da koduny giriziň:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                            </div>
                            <div class="another-options">
                                <div class="options-elements">
                                    <span>HARYDYŇ KODY</span>
                                    <select class="big-select" name="code" id="code" autocomplete="off">
                                        <option value="1">Harydyň koduny ýa-da adyny giriziň:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                                <div class="options-elements">
                                    <span>Harydyň görnüşi:</span>
                                    <select name="items" id="items" autocomplete="off">
                                        <option value="1">Gaplama görnüşi:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                            </div>
                        </div>
                        <div v-if="activeTab === 'tab2'">
                            <div class="text-title">
                                <span>ÝÜK GATNAWLARY ÜÇIN BAHA HASAPLAMAK</span>
                                <div class="text-option">
                                    <p>Ýük gatnawlary boýunça baha hasaplamak isleseňiz aşakdakylary doldurmak arkaly amala aşyryp bilersiňiz</p>
                                    <div class="options">
                                        <select name="options" id="options" class="select-1" autocomplete="off">
                                            <option value="1">TMT</option>
                                            <option value="2">$</option>
                                            <option value="3">TL</option>
                                        </select>
                                        <select name="dollars" id="dollars" autocomplete="off">
                                            <option value="1">Hojalyk jemgyyeti</option>
                                            <option value="2">$</option>
                                            <option value="3">TL</option>
                                        </select>
                                    </div>
                                </div>
                            </div>
                            <div class="two-options">
                                <div class="options-elements">
                                    <span>UGRAÝAN ÝURDY:</span>
                                    <select name="country" id="country" autocomplete="off">
                                        <option value="1">Stansiýanyň adyny ýa-da koduny giriziň:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                                <div class="options-elements">
                                    <span>GIRIŞ NOKADY:</span>
                                    <select name="login" id="login" autocomplete="off">
                                        <option value="1">Stansiýanyň adyny ýa-da koduny giriziň:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                            </div>
                            <div class="two-options">
                                <div class="options-elements">
                                    <span>Nirä:</span>
                                    <select name="where" id="where" autocomplete="off">
                                        <option value="1">Stansiýanyň adyny ýa-da koduny giriziň:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                                <div class="options-elements">
                                    <span>HARYDYŇ KODY</span>
                                    <select name="code" id="code" autocomplete="off">
                                        <option value="1">Stansiýanyň adyny ýa-da koduny giriziň:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                            </div>
                            <div class="another-options">
                                <div class="options-elements">
                                    <span>HARYDYŇ KODY</span>
                                    <select class="big-select" name="codes" id="codes" autocomplete="off">
                                        <option value="1">Harydyň koduny ýa-da adyny giriziň:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                                <div class="options-elements">
                                    <span>Harydyň görnüşi:</span>
                                    <select name="items" id="items" autocomplete="off">
                                        <option value="1">Gaplama görnüşi:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                            </div>
                        </div>
                        <div v-if="activeTab === 'tab3'">
                            <div class="text-title">
                                <span>ÝÜK GATNAWLARY ÜÇIN BAHA HASAPLAMAK</span>
                                <div class="text-option">
                                    <p>Ýük gatnawlary boýunça baha hasaplamak isleseňiz aşakdakylary doldurmak arkaly amala aşyryp bilersiňiz</p>
                                    <div class="options">
                                        <select name="options" id="options" class="select-1" autocomplete="off">
                                            <option value="1">TMT</option>
                                            <option value="2">$</option>
                                            <option value="3">TL</option>
                                        </select>
                                        <select name="dollars" id="dollars" autocomplete="off">
                                            <option value="1">Hojalyk jemgyyeti</option>
                                            <option value="2">$</option>
                                            <option value="3">TL</option>
                                        </select>
                                    </div>
                                </div>
                            </div>
                            <div class="two-options">
                                <div class="options-elements">
                                    <span>UGRAÝAN ÝURDY:</span>
                                    <select name="country" id="country" autocomplete="off">
                                        <option value="1">Stansiýanyň adyny ýa-da koduny giriziň:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                                <div class="options-elements">
                                    <span>GIRIŞ NOKADY:</span>
                                    <select name="login" id="login" autocomplete="off">
                                        <option value="1">Stansiýanyň adyny ýa-da koduny giriziň:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                            </div>
                            <div class="two-options">
                                <div class="options-elements">
                                    <span>Nirä:</span>
                                    <select name="where" id="where" autocomplete="off">
                                        <option value="1">Stansiýanyň adyny ýa-da koduny giriziň:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                                <div class="options-elements">
                                    <span>HARYDYŇ KODY</span>
                                    <select name="code" id="code" autocomplete="off">
                                        <option value="1">Stansiýanyň adyny ýa-da koduny giriziň:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                            </div>
                            <div class="another-options">
                                <div class="options-elements">
                                    <span>HARYDYŇ KODY</span>
                                    <select class="big-select" name="codes" id="codes" autocomplete="off">
                                        <option value="1">Harydyň koduny ýa-da adyny giriziň:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                                <div class="options-elements">
                                    <span>Harydyň görnüşi:</span>
                                    <select name="items" id="items" autocomplete="off">
                                        <option value="1">Gaplama görnüşi:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                            </div>
                        </div>
                        <div v-if="activeTab === 'tab4'">
                            <div class="text-title">
                                <span>ÝÜK GATNAWLARY ÜÇIN BAHA HASAPLAMAK</span>
                                <div class="text-option">
                                    <p>Ýük gatnawlary boýunça baha hasaplamak isleseňiz aşakdakylary doldurmak arkaly amala aşyryp bilersiňiz</p>
                                    <div class="options">
                                        <select name="options" id="options" class="select-1" autocomplete="off">
                                            <option value="1">TMT</option>
                                            <option value="2">$</option>
                                            <option value="3">TL</option>
                                        </select>
                                        <select name="dollars" id="dollars" autocomplete="off">
                                            <option value="1">Hojalyk jemgyyeti</option>
                                            <option value="2">$</option>
                                            <option value="3">TL</option>
                                        </select>
                                    </div>
                                </div>
                            </div>
                            <div class="two-options">
                                <div class="options-elements">
                                    <span>UGRAÝAN ÝURDY:</span>
                                    <select name="country" id="country" autocomplete="off">
                                        <option value="1">Stansiýanyň adyny ýa-da koduny giriziň:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                                <div class="options-elements">
                                    <span>GIRIŞ NOKADY:</span>
                                    <select name="login" id="login" autocomplete="off">
                                        <option value="1">Stansiýanyň adyny ýa-da koduny giriziň:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                            </div>
                            <div class="two-options">
                                <div class="options-elements">
                                    <span>Nirä:</span>
                                    <select name="where" id="where" autocomplete="off">
                                        <option value="1">Stansiýanyň adyny ýa-da koduny giriziň:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                                <div class="options-elements">
                                    <span>HARYDYŇ KODY</span>
                                    <select name="code" id="code" autocomplete="off">
                                        <option value="1">Stansiýanyň adyny ýa-da koduny giriziň:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                            </div>
                            <div class="another-options">
                                <div class="options-elements">
                                    <span>HARYDYŇ KODY</span>
                                    <select class="big-select" name="codes" id="codes" autocomplete="off">
                                        <option value="1">Harydyň koduny ýa-da adyny giriziň:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                                <div class="options-elements">
                                    <span>Harydyň görnüşi:</span>
                                    <select name="items" id="items" autocomplete="off">
                                        <option value="1">Gaplama görnüşi:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                            </div>
                            <div class="another-options">
                                <div class="options-elements">
                                    <span>HARYDYŇ KODY</span>
                                    <select class="big-select" name="variant" id="variant">
                                        <option value="1">Harydyň koduny ýa-da adyny giriziň:</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Icon2 from '~/assets/railway/Icon (2).svg';
import ActiveIcon2 from '~/assets/railway/Icon (10).svg';
export default {
    data() {
        return {
            selectedPage: 'tabs', // Default to first page with tabs
            activeTab: 'tab1', // Default to the first tab
        };
    },
    computed: {
        bahaHasaplamakIcon() {
            return this.$route.path === '/logistika/yerli' ? ActiveIcon2 : Icon2;
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
    }
    .logistika{
        position: relative;
        .tabs {
            width: auto;
            height: 45px;
            display: flex;
            gap: 20px;
            margin: 0px 30px;
        }

        .tabs li {
            list-style: none;
            border-radius: 10px;
            border: 1px solid #3A4052;
            background: transparent;
            font-size: 16px;
            font-weight: 700;
            color: #3A4052;
            padding: 11px 30px;
            cursor: pointer;
        }
        .tabs li.active {
            background-color: #14509D; /* Example styling for active link */
            border: none;
            color: white;
            font-size: 16px;
            font-weight: 700;
        }
        .text-title{
            margin-left: 30px;
            margin-top: 25px;
            span{
                font-size: 32px;
                font-weight: 800;
                color: #3A4052;
            }
            .text-option{
                display: flex;
                align-items: center;
                margin-top: 20px;
                gap: 70px;
                p{
                    width: 680px;
                }
                .options{
                    display: flex;
                    align-items: center;
                    gap: 10px;
                    .select-1{
                        width: 70px;
                        height: 40px;
                    }
                    select{
                        width: 154px;
                        height: 58px;
                        border: 1px solid #14509D;
                        border-radius: 6px;
                        appearance: none;
                        -webkit-appearance: none;
                        -moz-appearance: none;
                        background: url('~/assets/railway/Vector.svg') no-repeat right 10px center;
                        padding: 10px;
                        color:#14509D;
                        font-weight: 700;
                    }
                    select:focus {
                        border-color: #3498db;
                        outline: none;
                    }
                    option{
                        color:#14509D;
                        font-weight: 700;
                    }
                }
            }
        }
        .two-options{
            margin-top: 40px;
            margin-left: 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 1090px;
            gap: 30px;
            label{
                margin-bottom: 10px;
                font-size: 14px;
                font-weight: 600;
                color: #3A4052;
                letter-spacing: 1.4px;
            }
            select{
                padding: 10px 15px;
                width: 530px;
                height: 47px;
                border-radius: 4px;
                border: 1px solid #C4C4C4;
                color: #3A4052;
                appearance: none;
                -webkit-appearance: none;
                -moz-appearance: none;
                background: url('~/assets/railway/Vector (3).png') no-repeat right 20px center;
            }
            .options-elements{
                display: flex;
                flex-direction: column;
            }
        }
        .another-options{
            margin-top: 20px;
            margin-left: 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 30px;
            label{
                margin-bottom: 10px;
                font-size: 14px;
                font-weight: 600;
                color: #3A4052;
                letter-spacing: 1.4px;
                text-transform: uppercase;
            }
            .big-select{
                padding: 10px 15px;
                width: 810px;
                height: 47px;
                border-radius: 4px;
                border: 1px solid #C4C4C4;
                color: #3A4052;
                appearance: none;
                -webkit-appearance: none;
                -moz-appearance: none;
                background: url('~/assets/railway/Vector (3).png') no-repeat right 20px center;
            }
            select{
                padding: 10px 15px;
                width: 250px;
                height: 47px;
                border-radius: 4px;
                border: 1px solid #C4C4C4;
                color: #3A4052;
                appearance: none;
                -webkit-appearance: none;
                -moz-appearance: none;
                background: url('~/assets/railway/Vector (3).png') no-repeat right 20px center;
            }
            .options-elements{
                display: flex;
                flex-direction: column;
            }
        }
    }
}
</style>