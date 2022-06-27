<template>
  <div class="service" id="service">
    <h1>Our services</h1>
    <div class="cards">
      <div class="card">
        <div class="content">
          <h2>Custom Colorways</h2>
          <p>Ai technology</p>
        </div>
      </div>
      <div class="card">
        <div class="content">
          <h2>Are you Ready</h2>
          <p>Take the Lepa</p>
        </div>
      </div>
      <div class="card">
        <div class="content">
          <h2>Full gradients</h2>
          <p>100 Combination</p>
        </div>
      </div>
      <div class="card">
        <div class="content">
          <h2>Infinite choices</h2>
          <p>1000's of colors</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.service {
  width: 100%;
  height: 100vh;
  background: linear-gradient(to left, rgb(49, 48, 48), black);
}
h1 {
  font-size: 65px;
  text-align: center;
  padding: 50px 0;
  background: linear-gradient(to right, #f5af19, #f12711);
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
.service .cards {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    padding: 0 35px 0 20px;
}
.service .card {
  height: 320px;
  margin-left: 15px;
  border: none;
  transition: 0.3s;
  cursor: pointer;
}
.service .card:nth-child(1) {
  background: linear-gradient(to right, #093028, #237A57);
}
.service .card:nth-child(2) {
  background: linear-gradient(to right, #c31432, #240b36);
}
.service .card:nth-child(3) {
  background: linear-gradient(to right, #ffafbd, #ffc3a0);
}
.service .card:nth-child(4) {
  background: linear-gradient(to right, #44a08d, #093637);
}
.content{
     text-align: center;
     margin: auto auto;
}
.card h2 {
  color: white;
  font-size: 29px;
  font-family: sans-serif;
  font-weight: bold;
}
.card p {
  font-weight: 800;
  font-size: 24px;
  background: linear-gradient(to right, #f5af19, #f12711);
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
.service .card:hover{
    transform: scale(1.075);
    transition: 0.3s ease-in;
}
@media(max-width:1200px){
    .service{
        height: max-content;
    }
    .service .cards{
       grid-template-columns: 1fr 1fr;
    }
    .service .card{
        margin-top: 20px;
    }
}
@media(max-width:650px){
    .service .cards{
       grid-template-columns: 1fr ;
    }
}
</style>
