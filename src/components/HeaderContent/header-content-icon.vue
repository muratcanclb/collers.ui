<script setup lang="ts">

import contentIconShape1 from "../../assets/images/content/icon/content-icon-shape1.png";
import contentIconShape2 from "../../assets/images/content/icon/content-icon-shape2.png";
import contentIconShape3 from "../../assets/images/content/icon/content-icon-shape3.png";
import contentIcon1 from "../../assets/images/content/icon/content-icon1.png";
import contentIcon2 from "../../assets/images/content/icon/content-icon2.png";
import contentIcon3 from "../../assets/images/content/icon/content-icon3.png";
</script>


<template>
    <div>
        <VRow>
            <VCol cols="12" md="4">
                <div class="container">
                    <div class="background-image">
                        <VImg :src="contentIcon1" alt="Main Image" class="main-image" />
                        <VImg :src="contentIconShape1" alt="Overlay Image" class="overlay-image" />
                    </div>
                </div>
                <h3 style="text-align: center;">Nibh rivirera</h3>
                <p style="text-align: left; padding: 3px; margin: 7%; ">Cancun is back, better than ever! Over a hundred
                    Mexico resorts have reopened and the state
                    tourism minister</p>
            </VCol>
            <VCol cols="12" md="4">
                <div class="container">
                    <div class="background-image">
                        <VImg :src="contentIcon2" alt="Main Image" class="main-image" />
                        <VImg :src="contentIconShape2" alt="Overlay Image" class="overlay-image" />
                    </div>
                </div>
                <h3 style="text-align: center;">Cursus amet</h3>
                <p style="text-align: left; padding: 3px; margin: 7%; ">Cancun is back, better than ever! Over a hundred
                    Mexico resorts have reopened and the state
                    tourism minister reopened and the state
                    tourism ministe</p>
            </VCol>
            <VCol cols="12" md="4">
                <div class="container">
                    <div class="background-image">
                        <VImg :src="contentIcon3" alt="Main Image" class="main-image" />
                        <VImg :src="contentIconShape3" alt="Overlay Image" class="overlay-image" />
                    </div>
                </div>
                <h3 style="text-align: center;">Molestiae dolore</h3>
                <p style="text-align: left; padding: 3px; margin: 7%; ">olestias id nostrum\nexcepturi molestiae dolore
                    omnis repellendus quaerat saepe\nconsectetur iste
                    quaerat
                    tenetur asperiores accusamusstrum\nexcepturi molestiae dolore omnis repellendu</p>
            </VCol>
        </VRow>
    </div>
</template>
<style scoped>
.container {
    position: relative;
    width: 100%;
    max-width: 25px;
    /* İsteğe bağlı olarak maksimum genişlik ayarlayabilirsiniz */
    margin: 0 auto;
    /* Ortalamak için */
}

.background-image {
    position: relative;
    width: 100%;
}

.main-image,
.overlay-image {
    width: 100%;
    height: auto;
}

.overlay-image {
    position: absolute;
    top: 0;
    left: 10px;
    right: 4px;
    width: 100%;
}

.v-card {
    border: 1px solid #ccc;
    border-radius: 8px;
    overflow: hidden;
}

.v-card-content {
    padding: 20px;
    background-color: transparent;
    /* Arka plan rengini tamamen saydam yapar */
}
</style>
