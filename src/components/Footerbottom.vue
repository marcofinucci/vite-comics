<script>
export default {
  name: "Footerbottom",
};
</script>

<template>
  <h3>{{ menu.title }}</h3>
  <nav>
    <ul>
      <li v-for="link in menu.links" :key="link.text">
        <a :href="link.url">{{ link.text }}</a>
      </li>
    </ul>
  </nav>
</template>

<style scoped>
h3 {
  font-size: 1.125rem;
  font-weight: 700;
  text-transform: uppercase;
  margin: 1.5rem 0 0.75rem 0;
}

a {
  font-size: 0.875rem;
  padding: 0.25rem 0;
  color: #d2d2d2;
  transition: color 0.3s;
}

a.active,
a:hover {
  color: white;
  text-decoration: underline;
}
</style>
