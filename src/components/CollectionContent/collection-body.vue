<script lang="ts">
import panel from "../../assets/images/collection/panel.png";
import wave from "../../assets/images/collection/wave.png";
import collectionMap from "./collection-map.vue";

export default {
    components: {
        collectionMap
    },
    data() {
        return {
            items :[
                { title: 'My Files', value: 1, prependIcon: 'tabler-folder' },
                { title: 'Shared with me', value: 2, prependIcon: 'tabler-users' },
                { title: 'Starred', value: 3, prependIcon: 'tabler-star' },
                { title: 'Recent', value: 4, prependIcon: 'tabler-history' },
                { title: 'Offline', value: 5, prependIcon: 'tabler-circle-check' },
                { title: 'Uploads', value: 6, prependIcon: 'tabler-upload' },
                { title: 'Backups', value: 7, prependIcon: 'tabler-cloud-upload' },
            ],
            wave:wave,
            panel:panel
        }
    }
}

</script>
<template>
    <div>
        <div class="background-div" :style="{ backgroundImage: `url(${wave})` }" style="z-index: 2;">
            <VRow>
                <VCol cols="12">
                    <span style="color: black;">
                        <h1>Grow your collection</h1>
                    </span>
                </VCol>
            </VRow>
            <VRow>
                <VCol cols="12">
                    <span>Phasellus in nulla at lacus placerat sodales sed vitae lorem. Lorem ipsum dolor sit amet,
                        consectetur adipiscing elit.
                        iaculis. </span>
                </VCol>
            </VRow>
            <VRow>
                <VCol cols="12" md="6">
                    <VList nav :lines="false" width="170px" style="margin-bottom: 30%;">
                        <VListItem v-for="item in items" :key="item.value" :value="item.value">
                            <template #prepend>
                                <VIcon style="color: black;" :icon="item.prependIcon" class="me-3" />
                            </template>

                            <VListItemTitle>
                                <span style="color: black;">{{ item.title }}</span>
                            </VListItemTitle>
                        </VListItem>
                    </VList>
                </VCol>
                <VCol cols="12" md="6">
                    <VImg :src="panel"></VImg>
                </VCol>
            </VRow>
        </div>
        <collectionMap></collectionMap>

    </div>
</template>
<style lang="scss" scoped>
.background-div {
    width: 100%;
    /* Div genişliği */
    height: auto;
    /* Div yüksekliği */
    //background-image: url(wave); /* Arka plan resmi URL'si */
    background-size: cover;
    /* Arka plan resminin div içinde tamamen kaplanmasını sağlar */
    //background-position: center; /* Arka plan resminin ortalanmasını sağlar */
    background-position: center bottom;
    position: relative;

    //display: flex;
    justify-content: center;
    align-items: center;

}
</style>