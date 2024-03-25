<script setup lang="ts">
import mapMark from "../../assets/images/collection/map-mark.png";
import map from "../../assets/images/collection/map.png";
</script>
<template>
    <div class="container">
        <div class="bg-image" :style="{ backgroundImage: `url(${map})` }" style="background-color: #78350F;">
            <VImg :src="mapMark" class="overlay-image"></VImg>
  
            <VRow>
                <VCol class="text" cols="12" md="12" sm="12" style="text-align: center; padding-bottom: 1px;">
                    <h1 style="color: white; margin-bottom: 1px; font-size: 30px;">11,658,467</h1><br>
                </VCol>
                <VCol class="text" cols="12" md="12" sm="12" style="text-align: center; padding-top: 1px;">
                    <h1 style="color: white; margin-top: 1px; font-size: 30px;">Shoes Collected</h1>
                </VCol>
            </VRow>
        </div>
    </div>
</template>
<style lang="scss" scoped>
.bg-image {
    width: 100%;
    height: 400px;
    //height: 717px;
    background-color: #78350f;
    color: #fffbeb;
    //background-image: url(/assets/world-DxUAioIN.png);
    background-repeat: no-repeat;
    //background-size: cover;
    background-position: center;
    display: flex;
    justify-content: center;
    align-items: center;
}

.container {
    position: relative;
    width: 100%;
    height: 400px;
    /* Container yüksekliği */
}

.overlay-image {
    position: absolute;
    top: 20%;
    left: 35%;
    transform: translate(30%, -50%);
    width: 100px;
    /* Üstteki resmin genişliği */
    height: auto;
}
</style>