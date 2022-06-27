<template>
  <div class="nav fixed-top">
    <div class="container">
      <div class="nav-logo">
        <a href="#home" class="logo" >Gradient</a>
      </div>
      <div class="links">
        <ul class="ul-links">
          <li>
            <a href="#home" id="home-page"> Home</a>
          </li>
          <li>
            <a href="#about" id="about-page">About</a>
          </li>
          <li>
            <a href="#service" id="service-page">Service</a>
          </li>
          <a href="#sign"><button class="btn">Sign Up</button></a>
        </ul>
        <div id="one-toggle" class="toogle">
          <ul class="ul-toogle">
            <li>
              <a href="#home" @click="hiddenmenu"> Home</a>
            </li>
            <li>
              <a href="#about" @click="hiddenmenu">About</a>
            </li>
            <li>
              <a href="#service" @click="hiddenmenu">Service</a>
            </li>
            <a href="#sign" @click="hiddenmenu"
              ><button class="btn">Sign Up</button></a
            >
          </ul>
        </div>
        <div class="bar">
          <span class="span"></span>
          <span class="span"></span>
          <span class="span"></span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    let mybtn = document.querySelector(".bar");
    let mytoogle = document.getElementById("one-toggle");

    mybtn.addEventListener("click", function () {
      mytoogle.classList.toggle("active");
      this.classList.toggle("activate");
    });
  },
  //Do not work yet
  methods: {
    highlight(){
      let elem = document.querySelector(".highlight");
      let myhome = document.getElementById("home-page");
      let myabout = document.getElementById("about-page");
      let myservice = document.getElementById("service-page");
      let position = window.scrollY;

      if (window.innerWidth > 850 && position < 600) {
        myhome.classList.add("highlight");
        myabout.classList.remove("highlight");
        return;
      } else if (window.innerWidth > 850 && position < 1400) {
        myabout.classList.add("highlight");
        myhome.classList.remove("highlight");
        myservice.classList.remove("highlight");
        return;
      } else if (window.innerWidth > 850 && position < 2345) {
        myservice.classList.add("highlight");
        myabout.classList.remove("highlight");
        return;
      }
      if ((elem && window.innerWidth < 850 && position < 600) || elem) {
        elem.classList.remove("highlight");
      }
    },
  },
  methods: {
    hiddenmenu() {
      let mybtn = document.querySelector(".bar");
      let mytoogle = document.getElementById("one-toggle");

      mybtn.classList.toggle("activate");
      mytoogle.classList.remove("active");
    },
  },
};
</script>

<style scoped>
.nav {
  width: 100%;
  height: 80px;
  background-color: black;
  display: flex;
  padding: 0 50px;
}
@media (max-width: 600px) {
  .nav {
    padding: 0 10px;
  }
  .nav-logo .logo {
    font-size: 35px;
  }
}
.container {
  display: flex;
  justify-content: space-between;
  width: 100%;
}
.nav-logo {
  display: flex;
  align-items: center;
}
.nav-logo a {
  font-size: 45px;
  text-decoration: none;
  font-weight: 800;
  font-family: sans-serif;
  background: #f12711;
  background: linear-gradient(to right, #f5af19, #f12711);
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
.links {
  display: flex;
}
.links .ul-links {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 400px;
  margin-bottom: 0;
}
.links li {
  list-style: none;
}
.links .ul-links a {
  text-decoration: none;
  color: white;
  font-size: 21px;
  transition: 0.4s;
  font-family: sans-serif;
  position: relative;
}
.links .ul-links a:hover {
  color: #f5af19;
}
.btn {
  padding: 10px;
  color: white;
  font-size: 21px;
  font-family: sans-serif;
  cursor: pointer;
  border: none;
  border-radius: 5px;
  background: #f12711;
  background: -webkit-linear-gradient(to right, #f5af19, #f12711);
  background: linear-gradient(to right, #f5af19, #f12711);
}
.bar {
  margin: auto;
  cursor: pointer;
}
.bar span {
  width: 30px;
  height: 3px;
  margin: 5px 0;
  background: white;
}
.links .toogle {
  display: none;
}
@media (max-width: 850px) {
  .links .ul-links {
    display: none;
  }
  .links .toogle {
    display: block;
    width: 300px;
    height: 400px;
    margin-top: 80px;
    position: fixed;
    right: -300px;
    background-color: black;
    transition: 0.5s;
    z-index: 100;
  }
  .links .toogle.active {
    right: 0;
  }
  .links .toogle .ul-toogle {
    text-align: center;
  }
  .links .toogle .ul-toogle li {
    margin-top: 25px;
    list-style: none;
  }
  .links .toogle .ul-toogle a {
    color: white;
    list-style: none;
    text-decoration: none;
    font-size: 21px;
  }
  .bar span {
    display: block;
    transition: 0.5s;
  }
  .bar.activate .span:nth-child(2) {
    opacity: 0;
  }
  .bar.activate .span:nth-child(1) {
    transform: translateY(8px) rotate(45deg);
  }
  .bar.activate .span:nth-child(3) {
    transform: translateY(-8px) rotate(-45deg);
  }
  .btn {
    margin-top: 30px;
  }
}
.highlight::after {
  content: "";
  width: 65px;
  height: 5px;
  background-color: #f12711;
  position: absolute;
  bottom: -30px;
  left: 0px;
}
</style>
