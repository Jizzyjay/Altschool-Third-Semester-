<template>
  <main class="error-container">
    <div class="image_wrapper">
      <img src="@/assets/404-landing-page-free-vector.jpg" />
    </div>
    <div class="errorText">
      <h1 class="errorHeading">
        4<span class="errorSpan">0</span>4 Page Not Found
      </h1>
      <router-link to="/" class="redirectHome"> Go Home</router-link>
    </div>
  </main>
</template>

<script>
export default {
  name: "ErrorPage",
};
</script>

<style>
.error-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 20px;
  height: calc(100vh - 80px);
  width: 98%;
  margin: 2rem 0;
  padding: 0 20px;
}

.image_wrapper {
  width: 400px;
  height: 300px;
  margin-top: 5rem;
}
.image_wrapper img {
  width: 100%;
}
.errorHeading {
  font-size: 48px;
  margin-top: 16px;
  margin-bottom: 16px;
  text-align: center;
  font-family: "Libre Baskerville", serif;
  font-weight: bolder;
}
.errorSpan {
  color: red;
}
.errorText {
  display: flex;
  flex-direction: column;
  gap: 20px;
  justify-content: center;
  align-items: center;
}

.error__msg {
  font-family: "Libre Baskerville", serif;
  font-size: 20px;
  text-align: center;
  color: red;
}
.errorSubMsg {
  font-family: "Libre Baskerville", serif;
  font-size: 26px;
  text-align: center;
}
.redirectHome {
  text-decoration: none;
  font-weight: 600;
  font-size: 18px;
  font-family: "Libre Baskerville", serif;
  color: white;
  background-color: #f7c04a;
  padding: 10px;
  border-radius: 10px;
}
.redirectHome:hover {
  background-color: #3f497f;
}

@media screen and (max-width: 768px) {
  .error-container {
    margin: 3rem 0;
  }
  .image_wrapper {
    width: 300px;
    height: 200px;
  }
  .errorHeading {
    font-size: 36px;
    padding: 0 1rem;
  }
  .errorSubMsg {
    font-size: 20px;
  }
  .error__msg {
    font-size: 16px;
  }
  .redirectHome {
    font-size: 16px;
  }
}
</style>
