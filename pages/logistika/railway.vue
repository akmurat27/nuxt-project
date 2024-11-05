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
                            <nuxt-link to="/logistika/railway" exact-active-class="active-aside-link">
                                <img :src="railwayIcon">
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
                                Üstaşyr ýük dasamak
                            </li>
                            <li @click="activeTab = 'tab2'" :class="{ active: activeTab === 'tab2' }">
                                Import we eksport
                            </li>
                            <li @click="activeTab = 'tab3'" :class="{ active: activeTab === 'tab3' }">
                                Gurluşyk we senagat
                            </li>
                        </ul>

                        <!-- Tab Content -->
                        <div v-if="activeTab === 'tab1'">
                            <div class="main-text">
                                <span> Ýükleri üstaşyr geçirmegiň <br> ýönekeýleşdirilen düzgünleri</span>
                                <p>Awtomatlaşdyrylan ulgam arkaly üstaşyr ýük geçirijiler mundan beýläk Türkmenistana gelmezden ýa-da şahamça açmazdan, ýüklerini resmileşdirip, töleglerini onlaýn usulda amala aşyryp bilerler. Täze ulgam arkaly Türkmenistanyň çäginde üstaşyr ýükleri yzarlamak mümkin.</p>
                            </div>
                            <div class="options">
                                <div class="btn">
                                    <h1>Giriş</h1>
                                </div>
                                <select name="options" id="options">
                                    <option value="option1">Опция 1</option>
                                    <option value="option2">Опция 2</option>
                                    <option value="option3">Опция 3</option>
                                </select>
                                <div class="btn">
                                    <h1>Çykyş:</h1>
                                </div>
                            </div>
                            <div class="txt">
                                <p>Bu sahypa diňe maglumatlar bilen tanyşmak üçin. Has anyk bahany hasaplamak üçin
                                    nusgada wagonyň görnüşini we agramyny (tonnada) görkeziň.</p>
                            </div>
                            <div class="overlay">
                                <div class="text">
                                    <span>Gysga maglumat</span>
                                </div>
                                <div class="text-items">
                                    <span>Türkmenistanyň çägi:km</span>
                                    <span>Ortaça wagty:</span>
                                    <span>Ýol nyrhy USD</span>
                                    <span>Goşmaça ýygymlar USD</span>
                                </div>
                            </div>
                        </div>
                        <div v-if="activeTab === 'tab2'">
                            <div class="text-title">
                                <span>SERHETDÄKI NOKATLAR</span>
                            </div>
                            <div class="options">
                                <div class="each-element">
                                    <span>Ýurt:</span>
                                    <select name="country" id="country" autocomplete="country">
                                        <option value="1">Опция 1</option>
                                        <option value="2">Опция 2</option>
                                        <option value="3">Опция 3</option>
                                    </select>
                                </div>
                                    
                                <div class="each-element change-size">
                                    <span>Nireden</span>
                                    <select name="from" id="from" autocomplete="from">
                                        <option value="1">Опция 2</option>
                                    </select>
                                </div>
                                    
                                <div class="each-element">
                                    <span>Nirä:</span>
                                    <select name="where" id="where" autocomplete="where">
                                        <option value="1">Опция 3</option>
                                    </select>
                                </div>
                                <div class="import-text">
                                    <span>Serhetýaka nokadymyz:</span>
                                </div>
                            </div>
                            <div class="text-item">
                                <span>Ýüküňizi soňky nokada barýança wagonlar bilen üpjün etmek</span>
                                <p>Gazagystana, Özbegistana, Russiýa Federasiýasyna, Eýrana we beýleki ýurtlara ýükleriňiziň iberilýän döwründe, wagonlar bilen üpjün etmek we olary halkara ylalaşyk esasynda mugt yzyna getirmek boýunça hyzmatlarymyz bar. Eksport edilýän harytlaryňyzyň soňky nokadyna eltilmesi üçin aşakdaky görnüşde wagonlar bilen üpjün edýäris.</p>
                            </div>
                            <div class="card-box">
                                <div class="card-box-div">
                                    <span class="card-main-element">Wagonlaryň görnüşleri:</span>
                                    <span class="card-element">Цистерна</span>
                                    <span>Крытый вагон</span>
                                    <span>Платформа</span>
                                    <span>Полувагон</span>
                                    <span>Вагон-термос</span>
                                </div>
                                <div class="card-box-div">
                                    <span class="card-main-element">BAHASY (TMT):</span>
                                    <span class="card-element">546,02</span>
                                    <span>546,02</span>
                                    <span>546,02</span>
                                    <span>546,02</span>
                                    <span>546,02</span>
                                </div>
                            </div>
                        </div>
                        <div v-if="activeTab === 'tab3'">
                            <div class="text-title">
                                <span>GURLUŞYK ÖNÜMLERI</span>
                                <p>BU SAHYPA DIŇE MAGLUMATLAR BILEN TANYŞMAK ÜÇIN. HAS ANYK BAHANA HASAPLAMAK ÜÇIN NUSGADA WAGONYŇ GÖRNÜŞINI WE AGRAMYNY (TONNADA) GÖRKEZIŇ.</p>
                            </div>
                            <div class="main-text-title">
                                <span>ÝÜK GATNAWLARY BILEN DÜRLI GÖRNÜŞ SENAGAT WE GURLUŞYK HARYTLARYNY GATNATMAK</span>
                                <p> 
                                    Ýurdumyzyň çäginde uly göwrümli taslamalary amala aşyrýan kärhanalar mundan beýläk ýükleriniň we enjamlarynyň gatnawlary üçin demir ýol ýük gatnawlaryndan giňden peýdalanyp bilerler. Kämilleşdirilen ulgam arkaly ýükleriň bellenilen senesinden gijä galman niýetlenilen nokada eltilmegi üpjün ediler. Bu bolsa alnyp barylýan senagat we gurluşyk taslamalarynyň bahalaryna we bellenilen möhletinde tamamlanmagyna oňaýly goşant goşar.
                                </p>
                                <p>
                                    «Demirýollary» AGPJ ýük gatnawlarynyň düzümindäki wagonlar arkaly dürli görnüşli senagat we gurluşyk harytlaryny gatnatmak mümkin. Şeýle hem, gurluşyk we senagat kärhanalary öz wagonlaryny ulanmak şerti bilen hem ýerine ýetirilýän hyzmatlardan peýdalanyp bilerler.
                                </p>
                                <p>
                                    • Gatnawy kyn we gymmat bolan agyr, göwrümi uly harytlar üçin çözgütler; <br>
                                    • Gurluşyk-gurnama işleriniň gatnaw harajatlaryny azaltmaga amatly çözgüt; <br>
                                    • Dürli görnüşli harytlar we enjamlar üçin wagonlar; <br>
                                    • Birža arkaly satylýan harytlaryň gatnawyny çalt hasaplap, bädeşlige ukyply söwdalaryguramak;
                                    <br>
                                    • Öz wagonlaryň arkaly ýükleri gatnatmak boýunça hyzmatdaşlyk.
                                </p>
                            </div>
                            <div class="overlay-card">
                                <div class="text">
                                    <span>TAKMYNAN BAHA</span>
                                </div>
                                <div class="text-items">
                                    <div class="elements">
                                        <span>ÝÜKÜŇ AGRAMY</span>
                                        <span>ARALYK</span>
                                        <span>ORTAÇA WAGT</span>
                                        <span>ÝOL NYRHY</span>
                                        <span>WAGON BILEN ÜPJÜN ETMEK</span>
                                        <span>STANSIÝA ÝYGYMLARY</span>
                                        <span class="bold-el">JEMI</span>
                                    </div>
                                    <div class="elements">
                                        <span class="bold-el">60 TONNA</span>
                                        <span class="bold-el">~1000 KM</span>
                                        <span class="bold-el">3 ДНЕЙ 6 ЧАС.</span>
                                        <span class="bold-el">TMT</span>
                                        <span class="bold-el">546.02 TMT</span>
                                        <span class="bold-el">~247.95 TMT </span>
                                        <span class="bold-el">~793.00 TMT</span>
                                    </div>
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
import Icon1 from '~/assets/railway/Vector(1).svg';
import ActiveIcon1 from '~/assets/railway/Icon(1).svg';
export default{
    data() {
        return {
            selectedPage: 'tabs', // Default to first page with tabs
            activeTab: 'tab1', // Default to the first tab
        };
    },
    computed: {
        railwayIcon() {
            return this.$route.path === '/logistika/railway' ? ActiveIcon1 : Icon1;
        },
        
    },
}
</script>

<style scoped lang="scss">
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
        .main-text{
            margin: 15px 30px;
            span{
                font-size: 30px;
                font-weight: 800;
                color: #3A4052;
                text-transform: uppercase;
                line-height: 55px
            }
            p{
                color: #3A4052;
                font-size: 18px;
                font-weight: 600;
                text-align: justify;
                width: 1107px;
            }
        }
        .options{
            display: flex;
            margin: 50px 30px;
            align-items: center;
            .btn{
                width: 80px;
                height: 56px;
                border-bottom: 1px solid #C4C4C4;
                color: #14509D;
                font-size: 10px;
                font-weight: 800;
            }
            select{
                width: 190px;
                height: 43px;
                border: 1px solid #14509D;
                border-radius: 6px;
                appearance: none;
                -webkit-appearance: none;
                -moz-appearance: none;
                background: url('~/assets/railway/Vector.svg') no-repeat right 10px center;
                margin: 0px 45px;
                padding: 10px;
            }
            select:focus {
                border-color: #3498db;
                outline: none;
            }
        }
        .txt{
            border-top: 1px solid #C4C4C4;
            width: 677px;
            height: 100px;
            margin: 65px 50px;
            p{
                color: #3A4052;
                font-size: 14px;
                font-weight: 400;
                line-height: 18px;
                margin-top: 20px;
                text-transform: uppercase;
            }
        }
        .overlay{
            position: absolute;
            top: 50%;
            left: 68%;
            width: 328px;
            height: 261px;
            border-radius: 4px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            .text{
                margin: 20px;
                span{
                    font-size: 16px;
                    font-weight: 800;
                    color: #3A4052;
                }
            }
            .text-items{
                border-top: 1px solid #C4C4C4;
                margin: 20px;
                display: flex;
                flex-direction: column;
                span{
                    margin-top: 20px;
                }
            }
        }
        .text-title{
            margin-left: 30px;
            margin-top: 20px;
            margin-bottom: 5px;
            span{
                font-size: 32px;
                font-weight: 800;
                color: #3A4052;
            }
        }
        .options{
            display: flex;
            margin: 10px 30px;
            align-items: end;
            .each-element{
                display: flex;
                flex-direction: column;
                color:#14509D;  
                font-weight: 800;
                font-size: 16px;
            }
            .change-size{
                margin: 0px 32px;
            }
            select{
                width: 190px;
                height: 43px;
                border: 1px solid #14509D;
                border-radius: 6px;
                appearance: none;
                -webkit-appearance: none;
                -moz-appearance: none;
                background: url('~/assets/railway/Vector.svg') no-repeat right 10px center;
                margin: 10px 0px;
                padding: 10px;
            }
            select:focus {
                border-color: #3498db;
                outline: none;
            }
            .import-text{
                padding-bottom: 15px;
                margin-left: 32px;
                span{
                    font-size: 16px;
                    font-weight: 800;
                    line-height: 36px;
                    color: #14509D;
                }
            }
        }
        .text-item{
            margin: 5px 30px;
            span{
                font-size: 32px;
                font-weight: 700;
                line-height: 44px;
                color: #3A4052;
            }
            p{
                font-size: 14px;
                font-weight: 400;
                line-height: 18px;
                color: #3A4052;
                width: 921px;
                text-transform: uppercase;
            }
        }
        .card-box{
            display: flex;
            margin: 25px 30px;
            .card-box-div{
                display: flex;
                flex-direction: column;
                margin-right: 60px;
                gap: 10px;
                .card-main-element{
                    margin-bottom: 18px
                }
                .card-element{
                    border-top: 1px solid #CFCFCF;
                    padding-top: 6px;
                }
            }
        }
        .text-title{
            margin-left: 30px;
            margin-top: 50px;
            margin-bottom: 5px;
            span{
                font-size: 32px;
                font-weight: 800;
                color: #3A4052;
                line-height: 62px;
            }
            p{
                width: 700px;
            }
        }
        .main-text-title{
            margin: 65px 30px;
            width: 666px;
            span{
                font-size: 32px;
                font-weight: 800;
                color: #3A4052;
                line-height: 44px;
            }
            p{
                width: 645px;
                margin-top: 20px;
            }
        }
        .overlay-card{
            position: absolute;
            top: 10%;
            left: 100%;
            width: 328px;
            height: 337px;
            border-radius: 4px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            .text{
                margin: 20px;
                span{
                    font-size: 16px;
                    font-weight: 800;
                    color: #3A4052;
                }
            }
            .text-items{
                border-top: 1px solid #C4C4C4;
                margin: 20px;
                display: flex;
                gap: 50px;
                .elements{
                    display: flex;
                    flex-direction: column;
                    gap: 15px;
                    margin-top: 10px;
                    span{
                        font-size: 12px;
                        font-weight: 400;
                        color:#3A4052;
                        width: 117px
                    }
                    .bold-el{
                        font-weight: 700;
                    }
                }
            }
        }
    }
}
</style>
