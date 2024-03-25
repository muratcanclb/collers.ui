<script>
import collectionContent from "../components/CollectionContent/collection-body.vue";
import feedbackContent from "../components/FeedbackContent/feedback-card-body.vue";
import footerContent from "../components/FooterContent/footer-content.vue";
import headerContent from "../components/HeaderContent/header-content-body.vue";
import joinContent from "../components/JoinContent/join-content-body.vue";
import mainContent from "../components/MainContent/main-card-body.vue";

export default {
  components: {
    headerContent,
    mainContent,
    joinContent,
    feedbackContent,
    footerContent,
    collectionContent,
  },
  data() {
    return {

    };
  }
}
</script>

<template>
  <div>
    <VRow>
      <VCol cols="12">
        <header-content></header-content>
      </VCol>
    </VRow>
    <VRow>
      <VCol cols="12"><main-content></main-content></VCol>
    </VRow>
    <VRow>
      <VCol cols="12">
        <join-content></join-content>
      </VCol>
    </VRow>
    <VRow>
      <VCol cols="12"><feedback-content></feedback-content></VCol>
    </VRow>
    <VRow>
      <VCol cols="12">
        <collection-content></collection-content>
      </VCol>
    </VRow>
    <VRow>
      <VCol cols="12" style="background-color: #0F172A;">
        <footer-content></footer-content>
      </VCol>
    </VRow>

  </div>
</template>
<style lang="scss">
.v-row {
  margin: 0px !important;
}
</style>
