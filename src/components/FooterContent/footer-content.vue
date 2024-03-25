<script setup lang="ts">
import appleStoreLogo from "../../assets/images/footer/appleStoreLogo.png";
import googlePlayLogo from "../../assets/images/footer/googlePlayLogo.png";
const items1 = ['Pricing', 'Overview', 'Browse', 'Accessibility', 'Five']
const items2 = ['Brainstorming', 'Ideation', 'Wireframing', 'Research', 'Design']
const items3 = ['Contact Us', 'Developers', 'Documentation', 'Integrations', 'Reports']
</script>

<template>
  <div>
    <VRow>
      <VCol cols="12" sm="6" md="3">
        <span style="color: white; padding-left: 15px;"><b>Product</b></span>
        <VList style="background-color: #0F172A; color: #BBC1CA;" :items="items1" />
      </VCol>
      <VCol cols="12" sm="6" md="3">
        <span style="color: white; padding-left: 15px;"><b>Solutions</b></span>
        <VList style="background-color: #0F172A; color: #BBC1CA;" :items="items2" />
      </VCol>
      <VCol cols="12" sm="6" md="3">
        <span style="color: white; padding-left: 15px;"><b>Support</b></span>
        <VList style="background-color: #0F172A; color: #BBC1CA;" :items="items3" />
      </VCol>
      <VCol cols="12" sm="6" md="3">
        <span style="color: white; padding-left: 15px;"><b>Get the App</b></span>
        <VRow>
          <VCol>
            <VImg style="width: 60px; height: 40px;" :src="appleStoreLogo"></VImg>
          </VCol>
        </VRow>
        <VRow>
          <VCol>
            <VImg style="width: 60px; height: 40px; margin-left: 0px;" :src="googlePlayLogo"></VImg>
          </VCol>
        </VRow>
        <VRow>
          <VCol><span style="color:white">Follow Us</span></VCol>
        </VRow>
        <VRow>
          <VCol cols="2"><v-icon style="color: white;" size="30">mdi-youtube</v-icon></VCol>
          <VCol cols="2"><v-icon style="color: white;" size="30">mdi-facebook</v-icon></VCol>
          <VCol cols="2"><v-icon style="color: white;" size="30">mdi-twitter</v-icon></VCol>
          <VCol cols="2"><v-icon style="color: white;" size="30">mdi-instagram</v-icon></VCol>
          <VCol cols="2"><v-icon style="color: white;" size="30">mdi-linkedin</v-icon></VCol>
        </VRow>
      </VCol>
    </VRow>
    <VRow>
      <VCol>
        <div class="line"></div>
      </VCol>
    </VRow>
    <VRow>
      
      <VCol cols="12" sm="6"> <span style="color: white;">Collers @ 2023. All rights reserved.</span></VCol>
      <VCol cols="12" sm="6">
       <div style="float: right;">
        <span style="color: white; margin: 10px;">Terms</span>
        <span style="color: white; margin: 10px;">Privacy</span>
        <span style="color: white; margin: 10px;">Contact</span>
        <span style="color: white; margin: 10px; "><v-icon style="color: white; margin: 5px 10px 15px 5px;" size="25">mdi-earth</v-icon>EN</span>
       </div>
      </VCol>
    </VRow>
  </div>
</template>

<style>
.line {
  width: 100%;
  height: 2px;
  /* Çizgi kalınlığı */
  background-color: #2A364A;
  /* Çizgi rengi */
}
</style>