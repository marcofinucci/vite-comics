<script>
export default {
  name: "Header",
  data() {
    return {
      menus: [
        {
          text: "Characters",
          url: "#",
        },
        {
          text: "Comics",
          url: "#",
          isActive: true,
        },
        {
          text: "Movies",
          url: "#",
        },
        {
          text: "Tv",
          url: "#",
        },
        {
          text: "Games",
          url: "#",
        },
        {
          text: "Collectibles",
          url: "#",
        },
        {
          text: "Videos",
          url: "#",
        },
        {
          text: "Fans",
          url: "#",
        },
        {
          text: "News",
          url: "#",
        },
        {
          text: "Shop",
          url: "#",
        },
      ],
    };
  },
};
</script>

<template>
  <header>
    <div class="container">
      <div class="inner">
        <div class="logo">
          <img src="/img/dc-logo.png" alt="DC Logo" />
        </div>
        <nav>
          <ul>
            <li v-for="menu in menus" :key="menu.title">
              <a v-bind:class="{ active: menu.isActive }" :href="menu.url">{{ menu.text }}</a>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
</template>

<style scoped>
.inner {
  display: flex;
  justify-content: space-between;
}

.logo {
  max-width: 75px;
  padding: 1rem 0;
}

nav ul {
  display: flex;
  gap: 2rem;
  height: 100%;
}

nav a {
  font-size: 0.875rem;
  font-weight: 700;
  display: block;
  height: 100%;
  display: flex;
  align-items: center;
  border-bottom: 4px solid transparent;
  transition: border 0.3s;
  text-transform: uppercase;
}

nav a.active,
nav a:hover {
  border-color: #0282f9;
  color: #0282f9;
}
</style>
