<template>
    <VRow>
        <VCol>
            <VCard>
                <VRow>
                    <VCol cols="12" md="6" style="padding: 5%;">
                        <h1 style="color: #0F172A;"><b>Why join us</b></h1>
                        <VList>
                            <VListItem v-for="(item, i) in items" :key="i" :value="item" rounded="shaped">
                                <template #prepend>
                                    <VIcon style="color: lightgreen;" :icon="item.icon" />
                                </template>
                                <!-- eslint-disable-next-line vue/no-v-text-v-html-on-component -->
                                <p>{{ item.text }}</p>
                            </VListItem>
                        </VList>
                        <VBtn variant="outlined">Sign up now</VBtn>
                    </VCol>
                    <VCol cols="12" md="6">
                        <VImg style="width: 80%; height: auto;" :src="videoImg"></VImg>
                    </VCol>
                </VRow>
            </VCard>
        </VCol>
    </VRow>
</template>
<script setup lang="ts">
import videoImg from "../../assets/images/videocard/videoImg.png";
const items = [
  { text: 'Cupcake sesame snaps dessert marzipan.', icon: 'tabler-check' },
  { text: 'Jelly beans jelly-o gummi bears chupa chups marshmallow.', icon: 'tabler-check' },
  { text: 'Bonbon macaroon gummies pie jelly',icon: 'tabler-check' },
]

</script>