<template>
  <!-- Booking Page -->
  <div v-if="BookingPage == true">
    <va-avatar color="success"> u </va-avatar>
    <!--map-->
    <div class="navbar"></div>
    <img
      src="https://arkinova.se/wp-content/uploads/2020/01/Vision-Ume%C3%A5-C-02.jpg"
      alt="logo"
      style="width: 20rem; height: 15rem; margin-top: 10px"
    />
    <h1>Enter Your Origin and Destination</h1>
    <form>
      <label for="origin">Origin:</label>
      <input type="text" id="origin" v-model="origin" /><br />

      <label for="destination">Destination:</label>
      <input type="text" id="destination" v-model="destination" /><br />

      <button type="submit" @click.prevent="submitForm()">Submit</button>
    </form>
    <!--Buttons-->
    <div class="container">
      <button
        class="button-default"
        @click="(BookingPage = false), (TimePage = true)"
      >
        Return
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
    <div class="navbar"></div>

    <h3>YOUR ORDER</h3>

    <div id="sumOfCart">
      <h4>Cab: W39SH</h4>
      Umeå Airport - Umeå Univerity
      <br />
      Pickup: 15.34
      <br /><br /><br />
      <h4>Total: 1390kr</h4>
    </div>
    <h3>CONTINUE WITH PAYMENT</h3>
    <div id="klarnaContainer">
      <img src="klarna2.png" alt="" />
    </div>

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
  <!-- time page -->
  <div v-else-if="TimePage == true">
    <div>
      <va-avatar color="success"> u </va-avatar>
      <div class="navbar"></div>
      <div class="button-container">
        <div class="title">Select time</div>
        <va-time-picker v-model="value" size="larger" />
      </div>
      <div class="container">
        <button class="button-default" @click="TimePage = false">
          Log out
        </button>
        <button
          class="button-default"
          @click="(TimePage = false), (BookingPage = true)"
        >
          Continue
        </button>
      </div>
    </div>
  </div>
  <!-- landing page -->
  <div v-else>
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
      <button class="button-fb" @click="TimePage = true">
        Continue with Facebook
      </button>
      <button class="button-google" @click="TimePage = true">
        Continue with Google
      </button>
      <button class="button-ios" @click="TimePage = true">
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
    ProfilePage: false,
    TimePage: false,
    selectedTime: null,
    origin: '',
    destination: '',
  }
}
,methods: {
  submitForm() {
    // Here you can submit the form data to your server or process it in some other way
    console.log('Form submitted!');
    console.log('Origin:', this.origin);
    console.log('Destination:', this.destination);
  }
}
     }
</script>
<script src="https://polyfill.io/v3/polyfill.min.js?features=default"></script>

<style>
#sumOfCart {
  width: 50%;
  height: 30vh;
  border-radius: 30px;
  background-color: #b9f5d8;
  margin: auto;
}
#klarnaContainer {
  width: 100%;
  height: 10vh;
}
#klarnaContainer img {
  width: 100%;
}
body {
  background-color: #d9fff5;
  padding: 0;
  margin: 0;
}
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 10vh;
}
.button-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 35vh;
  display: flex;
  flex-direction: column;
}
.button-fb {
  width: 15rem;
  height: 5rem;
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
  height: 5rem;
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
  height: 5rem;
  background-color: black;
  color: white;
  font-weight: bolder;
  border-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 20px;
}
.button-default {
  width: 15rem;
  height: 3rem;
  background-color: #6b8f71;
  color: #d9fff5;
  font-weight: bolder;
  border-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 20px;
}

.navbar {
  width: 100%;
  height: 4rem;
  background-color: #b9f5d8;
}
h3 {
  padding: 5rem;
}
h4 {
  padding: 3rem;
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
