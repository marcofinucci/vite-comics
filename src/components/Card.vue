<script>
export default {
  name: "Card",
  props: {
    card: Object,
  },
};
</script>

<template>
  <div class="card">
    <div class="image">
      <img :src="card.thumb" :alt="card.series" />
    </div>
    <h3>{{ card.series }}</h3>
  </div>
</template>

<style scoped>
.image {
  width: 100%;
  aspect-ratio: 1 / 1;
}

.image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: top;
}

h3 {
  color: white;
  margin-top: 1rem;
  text-transform: uppercase;
  font-size: 0.875rem;
}
</style>
