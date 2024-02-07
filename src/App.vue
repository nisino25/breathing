<template>
  <div class="solar-system">
    <div class="sun">
      <div class="sun-inner"></div>
    </div>
  </div>
</template>

<script>

  export default {
    name: 'App',
    components: {
    },
    data() {
      return {
        animate: true
      };
    },
    mounted() {
    },
  }
</script>

<style>
  html,body{
    background: #f7f7f5;
    margin: 0;
    padding: 0;
    background: #071d16;
  }
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    /* margin-top: 60px; */

    width: 700px;
    max-width: 100vw;
    margin: auto;
    /* border: 2px solid black; */
  }

  .solar-system{
    /* position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%); */

    display: block;
    width: 100%;
    height: 100vh;
    aspect-ratio: 1/1;

    
  }

  .sun-container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%; /* Adjust the height as needed */
    width: 100%;
    border: 2px solid red;
  }


  .sun{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);

    display: block;
    width: 50px;
    aspect-ratio: 1/1;

    background: #fbd277;
    border-radius: 50%;

    border: 1px solid   #483e26;

    transform-origin: 0% 0%; /* Ensure transformations scale from the center */
    animation: growAndShrink 19s infinite; 

    /* transform: scale(3) translate(-50%, -50%); */
  }

  .sun-inner{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);

    display: block;
    width: 75%;
    aspect-ratio: 1/1;

    background: #ffffff;
    border-radius: 50%;
    box-shadow: 0 0 8px 5px #fbd277; 
    box-shadow: 0 0 15px 10px #fbd277; 
  }

  @keyframes growAndShrink {
    0%, 100% { 
      transform: scale(1) translate(-50%, -50%);
    }
    21.05%, 57.9% { 
      transform: scale(2.5) translate(-50%, -50%);
    }
  }

  .grow-shrink-animation {
    animation: growAndShrink 19s infinite; /* Repeat indefinitely */
  }


</style>
