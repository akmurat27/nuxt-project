<template>
    <div>
        <div class="container">
            <div class="header">
                <span class="main-title">Logistika</span>
                /
                <span class="main-title-2">Deňiz ýük gatnawlary</span>
            </div>
            <div class="main-page">
                <div class="aside">
                    <div class="aside-header">
                        <span>Deňiz ýük gatnawlary</span>
                    </div>
                    <ul class="list">
                        <li>
                            <nuxt-link to="/logistika/deniz/deniz-gatnawy" exact-active-class="active-aside-link" class="nav-link">
                                <img src="~/assets/railway/Icon(1).svg">
                                Gämi hakynda maglumatlar
                            </nuxt-link>
                        </li>
                    </ul>
                </div>
                <div class="logistika">
                    <span>Gatnaw hakynda maglumat</span>
                    <p>Gämini saýlaň</p>
                    <div class="options">
                        <select name="options" id="options">
                            <option value="1"></option>
                            <option value="2">WAGONYŇ GÖRNÜŞI:</option>
                            <option value="3">WAGONYŇ GÖRNÜŞI:</option>
                        </select>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
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
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin-top: 25px;
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
                font-weight: 700;
                width: 273px;
                height: 61px;
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
            text-transform: uppercase;
        }
        p{
            font-size: 14px;
            font-weight: 600;
            color:#3A4052;
            margin-top: 10px;
            margin-bottom: 10px;
            text-transform: uppercase;
        }
        .options{
            select{
                width: 530px;
                height: 47px;
                padding: 0px 10px;
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
</style>