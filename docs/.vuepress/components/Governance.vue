<template>
  <div>
    <h1>Governance</h1>
    <p>Learn about Umee's on-chain governance processes</p>
    <div class="row two-columns">
      <menu-card
        v-for="(menu, index) in menus"
        :key="index"
        :img="menu.img"
        :title="menu.title"
        :text="menu.text"
        :link="menu.link"
        :flex="true"
      />
    </div>

  </div>
</template>

<script>
import MenuCard from "./MenuCard.vue";
export default {
  components: { MenuCard },
  data() {
    return {
      menus: [
        {
          img: "/img/docs-users-icon.png",
          title: "Governance Overview",
          text: "An introduction to Umee's governance processes",
          link: "/governance/governance-overview",
        },
        {
          img: "/img/docs-users-icon.png",
          title: "New Asset Listings",
          text: "Learn how to propose a new asset to be listed on Umee",
          link: "/governance/asset-listing",
        },
        {
          img: "/img/docs-users-icon.png",
          title: "Community DAO",
          text: "Learn how to get involved through Umee's Community DAO",
          link: "/governance/community-dao",
        },
        {
          img: "/img/docs-users-icon.png",
          title: "Validator DAO",
          text: "Learn about the DAO that handles the Umee Foundation's delegation decisions",
          link: "/governance/validator-dao",
        },
      ],
    };
  },
};
</script>

<style lang="css">
.card {
  display: flex;
}
</style>
