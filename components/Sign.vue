<template>
  <div class="sign" id="sign" >
    <div class="sign-content">
      <div class="desc">
        <h2>Join Our Team</h2>
        <h1>Sign Up Today</h1>
        <p>See what makes us different</p>
        <button>Sign Up</button>
      </div>
      <div class="img"><i class=" icon fa-solid fa-user-group"></i></div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.sign{
    width: 100%;
    height: 100vh;
    background-color: black;
}
.sign-content{
    display: flex;
    padding: 0 120px;
    justify-content: space-between;
    align-items: center;
    height: 100%;
}
.img {
    width: 345px;
    height: 410px;
    background: #ff7e5f;
    background: -webkit-linear-gradient(to right, #feb47b, #ff7e5f);
    background: linear-gradient(to right, #feb47b, #ff7e5f);
    border-radius: 5px;
}
.sign-content .icon{
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
     color: rgb(144, 5, 187);
}
.desc h1{
    margin-top: 10px;
    font-size: 50px;
    font-weight: 600;
    font-family: sans-serif;
    color: #f1117a;
}
.desc p{
    color: white;
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
    .sign{
       height: max-content;
       padding: 100px 0;
    }
    .sign-content{
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
    .desc button{
        margin-bottom: 20px;
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
