<template>
  <div id="q-app">
    <router-view />
  </div>
</template>
<script>
export default {
  name: 'App'
}
</script>

<style lang="scss">
#q-app {
  background-size: cover;
  height:100vh;
}

.parallaxHeader {
  margin-top:-100px;
  background:black;
  height:100%;
  position: relative;
}

.backgroundTint {
    filter:blur(5px) brightness(80%);
}

.headerText {
  position: absolute;
  top: 50%;
  left: 50%;
  margin-left:auto;
  margin-right:auto;
  transform: translate(-50%, -50%);

  h1 {
    font-size:calc(40px + 4vw);
  }
}

.body {
    width:80%;
    margin:auto;
}


.footer {
  background:black;
  height:100%;
  position:relative;
}

@media screen and (max-width: 720px) {
  .body {
    width:100%;
  }
}

</style>