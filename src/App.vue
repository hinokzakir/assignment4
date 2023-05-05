<template>
  <div class="navbar"></div>
  <!-- logo -->
  <img
    src="https://seeklogo.com/images/T/taxi-vehicle-sign-logo-04DAE3D598-seeklogo.com.png"
    alt="logo"
    style="width: 8rem; margin-top: 10px"
  />

  <div class="title">THE TAXI APP</div>
  <!-- buttons -->
  <div class="button-container">
    <div class="button-fb">Continue with facebook</div>
    <div class="button-google">Continue with Google</div>
    <div class="button-ios">Continue with Apple</div>
  </div>
</template>

<script>
export default {
  name: 'App',
};
</script>

<style>
body {
  background-color: #d9fff5;
  padding: 0;
  margin: 0;
}
.button-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 20vh;
  display: flex;
  flex-direction: column;
}
.button-fb {
  width: 15rem;
  height: 6rem;
  background-color: #1877f2;
  color: white;
  font-weight: bolder;
  border-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.button-google {
  width: 15rem;
  height: 6rem;
  background-color: white;
  border-style: solid;
  color: black;
  font-weight: bolder;
  border-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 20px;
}

.button-ios {
  width: 15rem;
  height: 6rem;
  background-color: black;
  color: white;
  font-weight: bolder;
  border-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 20px;
}
.navbar {
  width: 100%;
  height: 5rem;
  background-color: #b9f5d8;
}
.footer {
  width: 100%;
  height: 5rem;
  background-color: #b9f5d8;
  position: absolute;
  bottom: 0;
}
.title {
  color: black;
  font-size: 3rem;
  font-weight: bolder;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
