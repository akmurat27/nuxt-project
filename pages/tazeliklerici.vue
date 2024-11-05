<template>
    <div class="image-switcher">
        <div class="active-image">
        <!-- Hardcoded Active Image 1 -->
        <img
            v-if="activeIndex === 0"
            src="~/assets/manager/Rectangle 74.png"
            alt="Selected Image 1"
        />
        <!-- Hardcoded Active Image 2 -->
        <img
            v-if="activeIndex === 1"
            src="~/assets/manager/main photo (1).png"
            alt="Selected Image 2"
        />
        <!-- Hardcoded Active Image 3 -->
        <img
            v-if="activeIndex === 2"
            src="~/assets/manager/main photo (2).png"
            alt="Selected Image 3"
        />
        <img
            v-if="activeIndex === 3"
            src="~/assets/manager/main photo (3).png"
            alt="Selected Image 4"
        />
        </div>
        
        <div class="thumbnail-grid">
        <!-- Hardcoded Thumbnail 1 -->
        <div
            @click="setActiveImage(0)"
            :class="['thumbnail', { 'active': activeIndex === 0 }]"
        >
            <img src="~/assets/manager/Rectangle 74.png" alt="Thumbnail 1" />
        </div>

        <!-- Hardcoded Thumbnail 2 -->
        <div
            @click="setActiveImage(1)"
            :class="['thumbnail', { 'active': activeIndex === 1 }]"
        >
            <img src="~/assets/manager/main photo (1).png" alt="Thumbnail 2" />
        </div>

        <!-- Hardcoded Thumbnail 3 -->
        <div
            @click="setActiveImage(2)"
            :class="['thumbnail', { 'active': activeIndex === 2 }]"
        >
            <img src="~/assets/manager/main photo (2).png" alt="Thumbnail 3" />
        </div>

        <!-- Hardcoded Thumbnail 4 -->
        <div
            @click="setActiveImage(3)"
            :class="['thumbnail', { 'active': activeIndex === 3 }]"
        >
            <img src="~/assets/manager/main photo (3).png" alt="Thumbnail 4" />
        </div>
        </div>

        <div class="tazelikler-text">
            <span>2024-nji ýylda Halkara logistika bazary nähili bolar</span>
            <p class="cislo">09.09.2024ý</p>
            <p>
                Türkmenistanyň yklymara ulag ýollarynyň geografik taýdan amatly çatrygynda ýerleşýändigini göz öňünde tutup, «Hazar logistika» hojalyk jemgyýetimiziň esasy maksady müşderiler üçin ýokary derejeli logistika hyzmatlaryny amala aşyrmak bolup durýar. Türkmenistanyň Ýewraziýa döwletleri bilen özara bähbitli gatnaşyklaryösdürmekde, şonuň ýaly-da, ýurdumyzyň milli ulag-aragatnaşyk ulgamyny örän netijelihem-de amatly peýdalanmakda döredýän giň mümkinçiliklerinden peýdalanyp, biziň agzybir toparymyz deňiz, awtoulag, demir ýol, howa gatnawlary esasynda ýerli, import, eksport we üstaşyr ýük gatnaw hyzmatlaryny amala aşyrýar. Biziň baş maksadymyz müşderileriň isleglerini doly kanagatlandyrmakdan we döwrebap hyzmatlary size hödürlemekden ybaratdyr.
            </p>
            <p class="text-2">
                Ulag — bu ykdysady sebitleriň toplumlaýyn ösdürilmeginde, öndüriji güýçleri çäk boýunça mümkingadar endigan ýerleşdirmekde, önümçilik pudaklarynyň, kärhanalaryň arasynda ykdysady, tehnologik aragatnaşygy amala aşyrmakda taýsyz serişdedir.Dünýä ýüzünde häzirki döwürde ulag ýollarynyň köpugurlylygy, hili we tizligi esasy görkezijileriň biri bolmak bilen, halkara ykdysady gatnaşyklarda aýgytly orun eýeleýär. Dünýä tejribesine syn salsak, geografik taýdan amatly ýerleşen ýurtlarda we sebitlerde ösen ulag toplumynyň döredilmegi üstaşyr ýüklerden hem goşmaça girdeji almaga mümkinçilik berýär. «Hazar logistik» hojalyk jemgyýetimiz hem her bir müşderiniň işiniň ösmegine özüniň goşandyny goşýar.
            </p>
        </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        activeIndex: 0, // Default to the first image
      };
    },
    methods: {
      setActiveImage(index) {
        this.activeIndex = index;
      }
    }
  };
  </script>
  
  <style>
  
  </style>
  