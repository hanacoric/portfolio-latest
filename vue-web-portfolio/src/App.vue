<template>
  <BlackSection/>
  <WhiteSection/>
  <VideoCV/>
  <EndSection/>
</template>

<script>
import BlackSection from './components/BlackSection.vue'
import WhiteSection from './components/WhiteSection.vue'
import VideoCV from './components/VideoCV.vue'
import EndSection from './components/EndSection.vue'

export default {


  name: 'App',
  components: {
    BlackSection,
    WhiteSection,
    VideoCV,
    EndSection
  },

  data() {
    return {
      images: [
      require('./assets/images/child-labour-poster.jpg'),
      require('./assets/images/longhornbbq-poster_1.jpg')
      ],
      logos: [
        require('./assets/images/child-labour-logo.png'),
        require('./assets/images/longhornbbqlogojpg.jpg')
      ],
      websiteImages: [
        require('./assets/images/website2.png'),
        require('./assets/images/website3.png'),
        require('./assets/images/website4.png'),
        require('./assets/images/website5.png'),
        require('./assets/images/website6.png'),
        require('./assets/images/website.png')
      ],
      currentIndex: 0,
      currentIndexLogos: 0,
      currentIndexWebsite: 0,
      intervalId: null,
      intervalIdLogos: null,
      intervalIdWebsite: null
    };
  },
  mounted() {
    window.addEventListener('scroll', this.onScroll);
    this.startSlideshow();
    this.startLogosSlideshow();
    this.startWebsiteSlideshow();
  },
  methods: { 
   
    isInView(element) {
      const bounding = element.getBoundingClientRect();
      return (
        bounding.top >= 0 &&
        bounding.bottom <= (window.innerHeight || document.documentElement.clientHeight)
      );
    },
    onScroll() {
      const images = document.querySelectorAll('.fade-in-image');
      const line = document.querySelector('.line');
      const nextLine = document.querySelector('.next_line');
      line.classList.add('animate');
      nextLine.classList.add('animate');
      images.forEach(image => {
        if (this.isInView(image)) {
          image.classList.add('active');
        }
      });
    },
    startSlideshow() {
      const slideshowPosters = document.querySelector('.slideshow_posters');
      this.intervalId = setInterval(() => {
        slideshowPosters.src = this.images[this.currentIndex];
        this.currentIndex = (this.currentIndex + 1) % this.images.length;
      }, 2000);
    },
    startLogosSlideshow() {
      const slideshowLogos = document.querySelector('.slideshow_logos');
      this.intervalIdLogos = setInterval(() => {
        slideshowLogos.src = this.logos[this.currentIndexLogos];
        this.currentIndexLogos = (this.currentIndexLogos + 1) % this.logos.length;
      }, 2000);
    },
    startWebsiteSlideshow() {
      const slideshowWebsite = document.querySelector('.website_img');
      this.intervalIdWebsite = setInterval(() => {
        slideshowWebsite.src = this.websiteImages[this.currentIndexWebsite];
        this.currentIndexWebsite = (this.currentIndexWebsite + 1) % this.websiteImages.length;
      }, 2000);
    }
  },
  beforeUnmount() {
    clearInterval(this.intervalId);
    clearInterval(this.intervalIdLogos);
    clearInterval(this.intervalIdWebsite);
    window.removeEventListener('scroll', this.onScroll);
  }
  }
</script>

<style>
@font-face {
    font-family: belfastgrotesk;
    src: url(./assets/fonts/BelfastGroteskRegular.ttf) format("truetype");
  }

  @font-face {
    font-family: belfastgroteskbold;
    src: url(./assets/fonts/BelfastGroteskBold.ttf) format("truetype");
  }

  @keyframes fade-in {
    0% { opacity: 0; }
    100% { opacity: 1; }
  }

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: belfastgrotesk;
}

#app::-webkit-scrollbar {
    display: none;
  }


#app {
  background-color: black;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: belfastgrotesk;
  width: 100vw;
}
</style>
