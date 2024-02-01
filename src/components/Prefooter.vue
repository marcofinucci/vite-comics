<script>
export default {
  name: "Preefooter",
  data() {
    return {
      items: [
        {
          text: "Digital comics",
          img: "/img/buy-comics-digital-comics.png",
        },
        {
          text: "DC Merchandise",
          img: "/img/buy-comics-merchandise.png",
        },
        {
          text: "Subscriptions",
          img: "/img/buy-comics-subscriptions.png",
        },
        {
          text: "comics shop locator",
          img: "/img/buy-comics-shop-locator.png",
        },
        {
          text: "dc power visa",
          img: "/img/buy-dc-power-visa.svg",
        },
      ],
    };
  },
};
</script>

<template>
  <div class="prefooter">
    <div class="container">
      <div class="prefooter-inner">
        <div class="item" v-for="item in items" :key="item.text">
          <div class="icon">
            <img :src="item.img" :alt="item.text" />
          </div>
          <span>{{ item.text }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.prefooter {
  background-color: #0282f9;
  padding: 2.5rem 0;
}

.prefooter-inner {
  display: flex;
  justify-content: center;
  gap: 3rem;
  color: white;
}

.item {
  display: flex;
  color: white;
  align-items: center;
  text-transform: uppercase;
  font-size: 0.875rem;
  white-space: nowrap;
}

.icon {
  margin-right: 0.75rem;
  position: relative;
}

.icon img {
  width: 100%;
  max-width: 45px;
  max-height: 45px;
}
</style>
