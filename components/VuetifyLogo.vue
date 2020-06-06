<template>
  <img
    class="VuetifyLogo"
    alt="ISKCON"
    src="/iskcon.png"
  >
</template>

<style>
.VuetifyLogo {
  height:250px;
  width: 250px;
  transform: rotateY(560deg);
  animation: turn 3.5s ease-out forwards 1s;
}

@keyframes turn {
  100% {
    transform: rotateY(0deg);
  }
}
</style>
