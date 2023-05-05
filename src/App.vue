<template>
  <div class="navbar"></div>
  <!-- Booking Page -->
  <div v-if="BookingPage == true">
    <!--map-->
    <img
      src="https://arkinova.se/wp-content/uploads/2020/01/Vision-Ume%C3%A5-C-02.jpg"
      alt="logo"
      style="width: 100%; height: 20rem; margin-top: 10px"
    />
    <!--Buttons-->
    <div class="container">
      <button class="button-default" @click="BookingPage = false">
        Log out
      </button>
      <button
        class="button-default"
        @click="(BookingPage = false), (CheckOutPage = true)"
      >
        Book a ride
      </button>
    </div>
  </div>
  <!-- checkout page -->
  <div v-else-if="CheckOutPage == true">
    KÖP NUUUUU
    <div class="container">
      <button
        class="button-ios"
        @click="(CheckOutPage = false), (BookingPage = true)"
      >
        Cancel
      </button>
      <button class="button-ios">Purchase</button>
    </div>
  </div>
  <!-- landing page -->
  <div v-else>
    <!-- logo -->
    <img
      src="https://seeklogo.com/images/T/taxi-vehicle-sign-logo-04DAE3D598-seeklogo.com.png"
      alt="logo"
      style="width: 8rem; margin-top: 10px"
    />

    <div class="title">THE TAXI APP</div>
    <!-- buttons -->
    <div class="button-container">
      <button class="button-fb" @click="BookingPage = true">
        Continue with Facebook
      </button>
      <button class="button-google" @click="BookingPage = true">
        Continue with Google
      </button>
      <button class="button-ios" @click="BookingPage = true">
        Continue with Apple
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
};
export default {
  data() {
    return {
      BookingPage: false,
      CheckOutPage: false,
      ProfilePage: false
    }
  }
}
</script>
<script src="https://polyfill.io/v3/polyfill.min.js?features=default"></script>

<style>
body {
  background-color: #d9fff5;
  padding: 0;
  margin: 0;
}
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 20vh;
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
.button-default {
  width: 15rem;
  height: 6rem;
  background-color: #6b8f71;
  color: #d9fff5;
  font-weight: bolder;
  border-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 20px;
}
.navbar {
  width: 100%;
  height: 4rem;
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
