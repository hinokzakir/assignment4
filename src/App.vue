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
  <div class="button-fb">Continue with facebook</div>
  <div class="button-ios" style="margin-top: 1rem">Continue with Apple</div>
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
.button-fb {
  width: 15rem;
  height: 3rem;
  background-color: #1877f2;
  color: white;
  font-weight: bolder;
  border-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.button-ios {
  width: 15rem;
  height: 3rem;
  background-color: black;
  color: white;
  font-weight: bolder;
  border-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
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
