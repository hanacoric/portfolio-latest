<template>
    <section class="white_section">
      <div class ="projects">
        <p>Here are some of my projects :)</p>
      </div>
      <div class="posters" >
        <h1>// POSTERS // <br> // POSTERS // <br> // POSTERS //</h1>
        <img :src="frontImgOne" alt="longhorn bbq poster" ref="slideshow_posters" class="slideshow_posters">
      </div>
      <div class="logos">
        <h1>// LOGOS // <br> // LOGOS // <br> // LOGOS //</h1>
        <img :src="frontImgTwo" alt="loghorn bbq logo" ref="slideshow_logos" class="slideshow_logos">
      </div>
      <div class="website">
        <h1>// WEBSITE // <br> // WEBSITE // <br> // WEBSITE // </h1>
        <img :src="frontImgThree" alt="twebsite" ref="website_img" class="website_img">
      </div>
    </section>
</template>

<script>
export default ({
data() {
    return {
        frontImgOne: require ("../assets/images/longhornbbq-poster_1.jpg") ,
        frontImgTwo: require("../assets/images/longhornbbqlogojpg.jpg") ,
        frontImgThree: require ("../assets/images/website.png") 
    }
}

})
    
</script>

<style>
.white_section{
    height: 200vh;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
    background-color: white;
    font-size: 2em;
}

.white_section h1{
    font-family: belfastgroteskbold;
}

.projects {
    display: flex;
    flex-direction: column;
    justify-content:space-between;
    align-items: center;
    color: black;
    text-align: center;  
    height: min-content;
}

.posters{
    width: 80vw;
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;
    height: min-content;
}

.slideshow_posters{
    width: 300px;
    height: 398px;
}

.logos{
    width: 80vw;
    display: flex;
    flex-direction: row-reverse;
    justify-content: space-evenly;
    align-items: center;
    height: min-content;
}

.slideshow_logos{
    width: 300px;
    height: 278px;
}

.logos h2{
    width: fit-content;
}

.website{
    width: 80vw;
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;
    height: min-content;
}

.website h3{
    width: fit-content;
}

.website_img{
    width: 300px;
    height: 300px;
}

@media (max-width: 1000px) {
  .white_section {
    font-size: 1.5em;
    height: 190vh;
    padding: 2rem;
  }

  .white_section h1 {
    font-size: 1em;
    margin-bottom: 30px;
    margin-top: 30px;
  }

  .posters, .logos, .website {
    flex-direction: column;
    align-items: center;
  }

  .slideshow_posters{
    width: auto;
    height: 320px;
  }

  .slideshow_logos, .website_img {
    width: auto;
    height: 200px;
  }
}

</style>