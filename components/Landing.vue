<template>
  <div class="landing" id="home">
     <div class="landing-content">
         <h1>Choose your <span>Design</span></h1>
         <p>Unlimited your colors</p>
         <button><span>Exblore</span></button>
     </div>
  </div>
</template>

<script>
export default {
}
</script>

<style scoped>
.landing{
    width: 100%;
    height: 100vh;
    background: black;
    background: linear-gradient(to left, rgb(43, 41, 41), black);
}
.landing-content{
    top: 50%;
    left: 50%;
    position: absolute;
    transform: translate(-50%,-50%);
}
.landing-content h1{
    color: white;
    font-family: sans-serif;
    font-size: 55px;
}
.landing-content h1 span{
    background: linear-gradient(to right, #f5af19, #f12711);
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
}
.landing-content p{
    background: linear-gradient(to right, white, white, #e65545);
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
    font-family: sans-serif;
    font-size: 35px;
    padding-top: 20px;
    text-align: center;
    font-weight: 600;
}
.landing-content button{
    display: flex;
    text-align: center;
    margin: 30px auto 0;
    padding: 15px 40px;
    color: white;
    border: none;
    cursor: pointer;
    font-size: 21px;
    border-radius: 5px;
    background: linear-gradient(to right , #f5af19, #f12711 );
    position: relative;
    outline: none;
}
.landing-content button:after{
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 0;
    height: 100%;
    border-radius: 5px;
    background: #ff1ead81;
    transition: 0.5s;
}
.landing-content button:hover:after{
    width: 100%;
}
.landing-content span{
    z-index: 4;
}
@media(max-width:1100px){
    .landing-content h1{
        font-size: 50px;
    }
    .landing-content p{
        font-size: 35px;
    }
}
@media(max-width:900px){
    .landing-content{
        padding: 0;
        width: max-content;
    }
    .landing-content h1{
        font-size: 40px;
        text-align: center;
    }
    .landing-content p{
        font-size: 25px;
    }
    .landing-content button{
        padding: 10px 30px;
    }
}
@media(max-width:400px){
       .landing-content h1{
        font-size: 30px;
        text-align: center;
       }
      .landing-content p{
        font-size: 15px;
      }
}
</style>
