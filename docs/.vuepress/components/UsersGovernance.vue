<template>
  <div>
    <h1>Governance</h1>
    <p></p>
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
          title: "Voting",
          text: "Learn how to vote on Umee",
          link: "/users/governance/voting",
        },
        {
          img: "/img/docs-users-icon.png",
          title: "Creating a Proposal",
          text: "Learn how to propose changes to the Umee network",
          link: "/users/governance/creating-proposal",
        },
        {
          img: "/img/docs-users-icon.png",
          title: "Creating a New Asset Listing Proposal",
          text: "Learn how to request support for a new asset on Umee",
          link: "/users/governance/new-asset-listing-proposal",
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
