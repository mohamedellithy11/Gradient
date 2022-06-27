<template>
  <div class="footer">
    <div class="footer-content">
      <div class="about">
          <h2>About Us</h2>
        <div v-for="(item, index) in about" :key="index" class="links">
          <a href=""> {{ item.title }}</a>
        </div>
      </div>
      <div class="contact">
          <h2>Contact Us</h2>
        <div v-for="(item, index) in contact" :key="index" class="links">
          <a href=""> {{ item.title }}</a>
        </div>
      </div>
      <div class="video">
          <h2>Videos</h2>
        <div v-for="(item, index) in video" :key="index" class="links">
          <a href=""> {{ item.title }}</a>
        </div>
      </div>
      <div class="social-media">
          <h2 id="h2">Social Media</h2>
        <div class=" links social-media-content" >
          <a href=""><i class="fa-brands fa-facebook"></i> </a>
          <a href=""><i class="fa-brands fa-instagram"></i> </a>
          <a href=""><i class="fa-brands fa-twitter"></i></a>
          <a href=""><i class="fa-brands fa-linkedin-in"></i> </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items:[],
      about: [
        { title: "How it Works" },
        { title: "Testmonials" },
        { title: "Carrers" },
        { title: "Terms of Services" },
      ],
      contact: [
        { title: "contact" },
        { title: "support" },
        { title: "Destination" },
      ],
      video: [
        { title: "Submit Video" },
        { title: "Ambassadors" },
        { title: "Agency" },
      ],
    };
  },
};
</script>

<style scoped>
.footer {
  width: 100%;
  height: 230px;
  background:linear-gradient(to right , rgb(71, 70, 70) , black) ;
}
.footer-content {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  width: 100%;
  height: 100%;
  padding: 0 60px;
  text-align: center;
  align-items: center;
}
@media(max-width:800px){
    .footer{
        height: max-content;
        padding-bottom: 20px;
    }
    .footer-content{
        grid-template-columns: 1fr 1fr;
        padding: 0;
    }
    h2{
        margin-top: 40px;
    }
}
@media(max-width:400px){
    .footer-content{
        grid-template-columns: 1fr;

    }
}
.social-media-content a{
    display: block;
}
.footer-content a{
    color: white;
    font-size: 17px;
}
h2{
    background: linear-gradient(to right, #f5af19, #f12711);
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
}
.about h2{
    color: white;
    margin-bottom: 20px;
}
.contact h2{
    margin-bottom: 40px;
}
.video h2{
    margin-bottom: 40px;
}
</style>
