<script lang="ts">
import contentBack from "../../assets/images/content/content-back.png"
import contentSneaker from "../../assets/images/content/content-sneaker.png"
import headerContentIcon from "./header-content-icon.vue"
export default {
    components: {
        headerContentIcon
    },
    setup() {
        let contentBackUrl = contentBack
        let contentSneakerUrl = contentSneaker
        return { contentBack, contentSneakerUrl };
    }
}
</script>


<template>
    <div class="background">
        <VRow>
            <VCol cols="12" md="6">
                <VRow>
                    <h1 style="font-size: 40px; text-align: center; margin: 20px;">Collectible Sneakers</h1>
                </VRow>
                <VRow>
                    <p style="text-align: left; margin: 10px;">Cancun is back, better than ever! Over a hundred Mexico resorts have reopened and the state tourism minister reopened </p>
                </VRow>
                <VRow>
                    <VCol cols="6">
                        <VBtn style="float: left;" variant="outlined">Sign up now</VBtn>
                    </VCol>
                    <VCol cols="6">
                        <VBtn rounded variant="outlined" style="border: none; float: left;">
                            <VIcon style="margin: 5px;" icon="tabler-play" /><b>Watch Demo</b>
                        </VBtn>
                    </VCol>
                </VRow>
            </VCol>
            <VCol cols="12" md="6">
                <VImg style="align-items: center; height: 50%" :src="contentSneakerUrl"></VImg>
            </VCol>
        </VRow>
        <VRow>
            <header-content-icon></header-content-icon>
        </VRow>
    </div>
</template>
<style scoped>

.background {
    background-image: url('../../assets/images/content/content-back.png');
    /* Arka plan resmi yolu */
    background-size: cover;
    /* Resmin div'e tamamen sığmasını sağlar */
    background-position: center;
    /* Resmi ortalar */
    width: 100%;
    /* Genişlik */
    height: auto;
    /* Yükseklik */
    text-align: center;
    /* Metni ortalar */
    padding-top: 10px;
    /* Metni yukarıda ortalar */
    margin: 0px;
}
</style>
