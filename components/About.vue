<template>
  <div class="about" id="about" >
    <div class="about-content">
      <div class="img"><i class=" icon fas fa-layer-group"></i></div>
      <div class="desc">
        <h2>What Do We Do</h2>
        <h1>we help businesses scale</h1>
        <p>call to learn more about our services</p>
        <button >call us</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {

};
</script>

<style scoped>
.about{
    width: 100%;
    height: 100vh;
    background-color: black;
}
.about-content{
    display: flex;
    padding: 0 120px;
    justify-content: space-between;
    align-items: center;
    height: 100%;
}
.img {
    width: 345px;
    height: 410px;
    margin: 0;
    padding: 0;
    background: #ff7e5f;
    background: -webkit-linear-gradient(to right, #feb47b, #ff7e5f);
    background: linear-gradient(to right, #feb47b, #ff7e5f);
    border-radius: 5px;
}
.about-content .icon{
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 49;
    width: 100%;
    height: 100%;
    font-size: 12rem;
    color: white;
}
.desc h2{
    font-size: 40px;
    font-family: sans-serif;
    background: linear-gradient(to right, white, white, #e65545);
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
}
.desc h1{
    margin-top: 10px;
    font-size: 50px;
    font-family: sans-serif;
     background: linear-gradient(to right, #f5af19, #f12711);
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
}
.desc p{
    background: linear-gradient(to right, white, white, #e65545);
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
    font-family: sans-serif;
    font-size: 25px;
    padding-top: 10px;
    font-weight: 600;
}
.desc button {
    margin: 30px 0 0 0;
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
.desc button:after{
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 0;
    height: 100%;
    border-radius: 5px;
    background: #ff1ead81;
    transition: 0.3s;
}
.desc button:hover:after{
    width: 100%;
    z-index: -3;
}
 button:hover{
     z-index: 69;
}
@media(max-width:1100px){
    .about{
       height: max-content;
       padding: 100px 0;
    }
    .about-content{
        display: block;
        padding:  0 0 0 0;
    }
    .img{
        margin: auto auto 50px;
        display: flex;
    }
    .desc{
        text-align: center;
        margin: auto auto;
    }
}
@media(max-width:520px){

    .img{
        width: 1fr;
        width: 100%;
        height: 350px;
    }
    .desc h2{
        font-size: 25px;
    }
    .desc h1{
        font-size:30px ;
    }
    .desc p{
        font-size: 15px;
    }
}
</style>
