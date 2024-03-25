<script setup lang="ts">
import card1image from "../../assets/images/icard/card1image.png";
import card2image from "../../assets/images/icard/card2image.png";
import card3image from "../../assets/images/icard/card3image.png";
import bgrect from "../../assets/images/icard/bgrects.png";
</script>
<template>
  <VRow style="background-color: #0F172A;">
    <VCol cols="12" md="6">
      <h1 style="color: white;">The best of the best</h1>
    </VCol>
    <VCol cols="12" md="6">
      <VBtn variant="outlined"
        style="color: white; float: right; background-color: #0F172A;  width:60%; margin: 5px 20px;">Sign up
        now</VBtn>
    </VCol>
  </VRow>
  <div :style="{ backgroundImage: `url(${bgrect})` }" style="background-color: #0F172A; background-position: center;">
    <VRow>
      <VCol cols="12" sm="6" md="4">
        <VCard style="background-color: #0F172A;">
          <VImg :src="card1image" cover />
          <VCardItem>
            <VCardTitle style="color: white;">Title</VCardTitle>
          </VCardItem>
          <VCardText style="color: white;">
            Cancun is back, better than ever! Over a hundred Mexico resorts have reopened and the state tourism minister
          </VCardText>
          <VBtn variant="outlined" style="color: white; background-color: #0F172A;  width:80%; margin: 5px 20px;">
            <VIcon style="margin-right: 15px;" icon="tabler-shopping-cart" />Buy Now
          </VBtn>
        </VCard>
      </VCol>
      <VCol cols="12" sm="6" md="4">
        <VCard style="background-color: #0F172A;">
          <VImg :src="card2image" cover />
          <VCardItem>
            <VCardTitle style="color: white;">Title</VCardTitle>
          </VCardItem>
          <VCardText style="color: white;">
            Cancun is back, better than ever! Over a hundred Mexico resorts have reopened and the state tourism minister
          </VCardText>
          <VBtn variant="outlined" style="color: white; background-color: #0F172A;  width:80%; margin: 5px 20px;">
            <VIcon style="margin-right: 15px;" icon="tabler-shopping-cart" />Buy Now
          </VBtn>
        </VCard>
      </VCol>
      <VCol cols="12" sm="6" md="4">
        <VCard style="background-color: #0F172A;">
          <VImg :src="card3image" cover />
          <VCardItem>
            <VCardTitle style="color: white;">Title</VCardTitle>
          </VCardItem>
          <VCardText style="color: white;">
            Cancun is back, better than ever! Over a hundred Mexico resorts have reopened and the state tourism minister
          </VCardText>
          <VBtn variant="outlined" style="color: white; background-color: #0F172A;  width:80%; margin: 5px 20px;">
            <VIcon style="margin-right: 15px;" icon="tabler-shopping-cart" />Buy Now
          </VBtn>
        </VCard>
      </VCol>
    </VRow>
  </div>
</template>