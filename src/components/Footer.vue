<script>
import Prefooter from "./Prefooter.vue";
import Footermenu from "./Footermenu.vue";

export default {
  name: "Footer",
  components: {
    Prefooter,
    Footermenu,
  },
  data() {
    return {
      menus: [
        {
          title: "DC Comics",
          links: [
            {
              text: "Characters",
              url: "#",
            },
            {
              text: "Comics",
              url: "#",
            },
            {
              text: "Movies",
              url: "#",
            },
            {
              text: "TV",
              url: "#",
            },
            {
              text: "Games",
              url: "#",
            },
            {
              text: "Videos",
              url: "#",
            },
            {
              text: "News",
              url: "#",
            },
          ],
        },
        {
          title: "Shop",
          links: [
            {
              text: "Shop DC",
              url: "#",
            },
            {
              text: "Shop DC Collectibles",
              url: "#",
            },
          ],
        },
        {
          title: "DC",
          links: [
            {
              text: "Terms Of Use",
              url: "#",
            },
            {
              text: "Privacy policy (New)",
              url: "#",
            },
            {
              text: "Ad Choices",
              url: "#",
            },
            {
              text: "Advertising",
              url: "#",
            },
            {
              text: "Jobs",
              url: "#",
            },
            {
              text: "Subscriptions",
              url: "#",
            },
            {
              text: "Talent Workshops",
              url: "#",
            },
            {
              text: "CPSC Certificates",
              url: "#",
            },
            {
              text: "Ratings",
              url: "#",
            },
            {
              text: "Shop Help",
              url: "#",
            },
            {
              text: "Contact Us",
              url: "#",
            },
          ],
        },
        {
          title: "Sites",
          links: [
            {
              text: "DC",
              url: "#",
            },
            {
              text: "MAD Magazine",
              url: "#",
            },
            {
              text: "DC Kids",
              url: "#",
            },
            {
              text: "DC Universe",
              url: "#",
            },
            {
              text: "DC Power Visa",
              url: "#",
            },
          ],
        },
      ],
    };
  },
  computed: {
    menuCol1() {
      return this.menus.slice(0, 2);
    },
  },
};
</script>

<template>
  <Prefooter></Prefooter>
  <footer>
    <div class="container">
      <div class="inner">
        <div class="left">
          <div>
            <Footermenu v-for="menu in menuCol1" :key="menu.title" :menu="menu"></Footermenu>
          </div>
          <Footermenu :menu="menus[2]"></Footermenu>
          <Footermenu :menu="menus[3]"></Footermenu>
        </div>
        <div class="right">
          <img src="/img/dc-logo-bg.png" alt="logo" />
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped>
footer {
  background-image: url("/img/footer-bg.jpg");
  background-size: cover;
  background-position: center;
  color: white;
  overflow: hidden;
}

.inner {
  display: flex;
  justify-content: space-between;
  gap: 3rem;
}

.left {
  padding: 3rem 0 4.5rem;
  display: flex;
  gap: 32px;
}
.right {
  margin: -3rem 0;
}
</style>
