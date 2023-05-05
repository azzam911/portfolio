<template>
  <div class="about">
    <div class="imgs">
      <img :src="selectedItem" alt="frontend-imgs">
    </div>

    <div class="info">
      
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        imgs: [
        "https://p92.com/binaries/content/gallery/p92website/technologies/htmlcssjs-overview.png",
        "https://upload.wikimedia.org/wikipedia/commons/thumb/d/d5/CSS3_logo_and_wordmark.svg/1200px-CSS3_logo_and_wordmark.svg.png",
        "https://upload.wikimedia.org/wikipedia/commons/thumb/6/61/HTML5_logo_and_wordmark.svg/800px-HTML5_logo_and_wordmark.svg.png",
        "https://logos-world.net/wp-content/uploads/2023/02/JavaScript-Logo.png",
        "https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/1200px-Vue.js_Logo_2.svg.png",
        ],
        selectedItem: "https://saintlouis.kidsoutandabout.com/sites/default/files/html_css_javascript.jpeg"
      }
    },
    methods: {
      randomItem () {
        const randItem = Math.floor(Math.random() * this.imgs.length);
        this.selectedItem = this.imgs[randItem]
      
    }
    },
    created() {
      
      setInterval(() => this.randomItem(), 3000);
    }
    
  }
</script>
<style>
.imgs img {
    width: 600px;
    height: 600px;
}
@media screen and (max-width: 600px) {
  .imgs img {
    width: 100%;

  }
  
}
</style>