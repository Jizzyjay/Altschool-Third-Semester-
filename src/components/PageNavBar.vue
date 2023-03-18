<template>
  <nav>
    <div class="logo">
      <router-link to="/" class="linkTag">Home</router-link>
    </div>
    <div class="nav-links">
      <router-link to="/counter">Counter</router-link>
      <router-link to="/404">404 Page</router-link>
    </div>
  </nav>
</template>

<script>
export default {
  name: "PageNavBar",
};
</script>
<style>
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #539165;
  color: white;
  width: 100%;
  padding: 14px;
  margin: 0 auto;
  box-shadow: 1px 1px 3px #555;
}

.logo {
  font-size: 1.5rem;
  font-family: secFont;
  font-weight: light;
  letter-spacing: 2px;
  margin-left: 15px;
}

.logo a:hover {
  color: #000;
  font-weight: bolder;
  transition: all 0.4s;
}

.nav-links {
  display: flex;
  gap: 10px;
  justify-content: space-between;
  align-items: center;
  margin-right: 15px;
}

.nav-links a:hover {
  color: #000;
  font-weight: bolder;
  transition: all 0.4s;
}

.nav-links a {
  color: inherit;
  text-decoration: none;
  margin-right: 1rem;
  font-family: cursive;
  font-weight: bolder;
}
</style>
