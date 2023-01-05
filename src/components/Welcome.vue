<template>
  <v-container>
    <div class="area">
      <ul class="circles">
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
      </ul>
    </div>
    <v-layout text-center wrap>
      <v-flex mb-4 xs12>
        <h2 class="display-2 font-weight-bold mb-3 welcomeMessage"></h2>
        <!-- Dont  format on save  or other text editor -->
        <vue-typer
          :text="['Hello World!','Welcome to Yuma Shimizu’s Portfolio','Let’s Mouse down!!']"
          :repeat="Infinity"
          :shuffle="false"
          initial-action="typing"
          :pre-type-delay="70"
          :type-delay="70"
          :pre-erase-delay="2000"
          :erase-delay="250"
          erase-style="select-all"
          :erase-on-complete="false"
          caret-animation="blink"
        ></vue-typer>
        <p class="subheading font-weight-regular"></p>
        <h2 class="welcomeIconWrapper">
          <font-awesome-icon class="welcomeIcon" icon="angle-double-down" />
        </h2>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import { VueTyper } from "vue-typer";
export default {
  components: {
    VueTyper
  }
};
</script>

<style lang="scss">
h1,
h2,
h3,
h4,
p,
a {
  color: white;
}
.vue-typer {
  font-family: Copperplate, "Copperplate Gothic Light", fantasy;
  font-size: 4rem;
}

.vue-typer .custom.char.typed {
  color: #41b883;
}

.context {
  width: 100%;
  position: absolute;
  top: 50vh;
}
.welcomeMessage {
  margin-top: 40vh;
}
.welcomeIconWrapper {
  margin: 200px 0;
  .welcomeIcon {
    font-size: 6rem;
    animation: disappear 1s ease infinite;
    color: #41b883;
  }
}
.context h1 {
  text-align: center;
  color: #fff;
  font-size: 50px;
}
.area {
  top: 0;
  left: 0;
  position: fixed;
  width: 100%;
  height: 100vh;
}

.circles {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
}

.circles li {
  position: absolute;
  display: block;
  list-style: none;
  width: 50px;
  height: 50px;
  animation: animate 5s linear infinite;
  bottom: -150px;
}

.circles li:nth-child(1) {
  background: rgba(101, 55, 151, 0.7);
  left: 25%;
  border-radius: 50%;
  width: 80px;
  height: 80px;
  animation-delay: 0s;
}

.circles li:nth-child(2) {
  background: rgba(101, 55, 151, 0.7);
  left: 10%;
  border-radius: 50%;
  width: 50px;
  height: 50px;
  animation-delay: 2s;
  animation-duration: 12s;
}

.circles li:nth-child(3) {
  background: rgba(101, 55, 151, 0.7);
  left: 70%;
  border-radius: 50%;
  width: 50px;
  height: 50px;
  animation-delay: 4s;
}

.circles li:nth-child(4) {
  background: rgba(101, 55, 151, 0.7);
  left: 40%;
  border-radius: 50%;
  width: 60px;
  height: 60px;
  animation-delay: 0s;
  animation-duration: 18s;
}

.circles li:nth-child(5) {
  background: rgba(101, 55, 151, 0.7);
  left: 65%;
  border-radius: 50%;
  width: 50px;
  height: 50px;
  animation-delay: 0s;
}

.circles li:nth-child(6) {
  background: rgba(16, 79, 214, 0.7);
  left: 75%;
  width: 110px;
  height: 110px;
  animation-delay: 3s;
}

.circles li:nth-child(7) {
  background: rgba(16, 79, 214, 0.7);
  left: 35%;
  width: 150px;
  height: 150px;
  animation-delay: 7s;
}

.circles li:nth-child(8) {
  background: rgba(16, 79, 214, 0.7);
  left: 50%;
  width: 25px;
  height: 25px;
  animation-delay: 15s;
  animation-duration: 45s;
}

.circles li:nth-child(9) {
  background: rgba(16, 79, 214, 0.7);
  left: 20%;
  width: 15px;
  height: 15px;
  animation-delay: 2s;
  animation-duration: 35s;
}

.circles li:nth-child(10) {
  background: rgba(16, 79, 214, 0.7);
  left: 0%;
  width: 150px;
  height: 150px;
  animation-delay: 2s;
  animation-duration: 14s;
}
.circles li:nth-child(11) {
  background: rgba(54, 35, 100, 0.7);
  left: 55%;
  width: 120px;
  height: 120px;
  animation-delay: 2s;
  animation-duration: 11s;
}
.circles li:nth-child(12) {
  background: rgba(54, 35, 100, 0.7);
  left: 60%;
  width: 70px;
  height: 70px;
  animation-delay: 3s;
  animation-duration: 10s;
}
.circles li:nth-child(13) {
  background: rgba(54, 35, 100, 0.7);
  left: 10%;
  width: 120px;
  height: 120px;
  animation-delay: 5s;
  animation-duration: 9s;
}
.circles li:nth-child(14) {
  background: rgba(54, 35, 100, 0.7);
  left: 15%;
  width: 160px;
  height: 160px;
  animation-delay: 3s;
  animation-duration: 10s;
}
.circles li:nth-child(15) {
  background: rgba(54, 35, 100, 0.6);
  left: 55%;
  width: 30px;
  height: 30px;
  animation-delay: 1s;
  animation-duration: 7s;
}

@keyframes animate {
  0% {
    transform: translateY(0) rotate(0deg);
    opacity: 1;
  }

  100% {
    transform: translateY(-1000px) rotate(720deg);
    opacity: 0;
  }
}
@keyframes disappear {
  0% {
    opacity: 1;
  }

  100% {
    opacity: 0;
    transform: translateY(50px);
  }
}
</style>