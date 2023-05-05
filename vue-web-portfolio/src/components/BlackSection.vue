<template>
       <section class="black_section">
      <div class="intro">
        <h1>Hello, my name is</h1>
        <h2>HANA CORIC</h2>
        <h3>Welcome to my portfolio!</h3>
      </div>
      <div class="line"></div>
      <div class="BusinessCardBack">
        <img src="../assets/images/bc_back.jpg" alt="patrick bateman holding business card back" class="fade-in-image">
      </div> 
      <div class="info">
        <p>I am a Multimedia student currently studying at</p>
        <p>Business Academy SouthWest in Esbjerg, Denmark.</p>
      </div>
      <div class="next_line"></div>
      <div class ="BusinessCardFront">
        <img src="../assets/images/bateman.jpg" alt="patrick bateman holding business card front" class="fade-in-image">
      </div>
      <div class="goal">
        <p>I come from Croatia and my main goal is to work</p>
        <span>as a graphic designer or UX/UI designer</span>
      </div>    
    </section> 
</template>

<style>
.black_section::-webkit-scrollbar {
    display: none;
  }

.black_section{
    height: 330vh;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    background-color: black;
    overflow-y: scroll;
}

.intro {
    display: flex;
    flex-direction: column;
    justify-content:space-evenly;
    align-items: center;
    color: white;
    text-align: center;  
    height: 50vh;
    margin-top: 25vh;
}

.intro h1 {
    text-align: center;
    font-weight: lighter; 
    font-size: 2em;
    animation: fade-in 4s;
  }
  
.intro h2 {
    font-weight: bold;
    text-align: center;
    font-family: belfastgroteskbold;
    font-size: 5em;
    animation: fade-in 2s;
  }
  
  .intro h3 {
    text-align: center;
    font-weight: lighter;
    font-size: 2em;
    animation: fade-in 6s;
  }

  .line{
    background-color: white;
    opacity: 0;
    width: 4px;
    height: 510px;
    position: absolute;
    margin-top: 90vh;
  }

  .next_line{
    background-color: white;
    opacity: 0;
    width: 4px;
    height: 600px;
    position: absolute;
    margin-top: 200vh;
  }
  
  .line.animate , .next_line.animate{
    animation: fade-in 1s;
    opacity: 1;
  }

.info, .goal {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: white;
    height: min-content;
    text-align: center;
    font-size: 2em;
    margin-bottom: 25vh;
}

.BusinessCardBack {
    height: min-content;
    width: 80vw;
    background-color: black;
}

.BusinessCardFront {
    display: flex;
    height: min-content;
    width: 80vw;
    justify-content: right;
    background-color: black; 
}

.fade-in-image {
    opacity: 0;
}

.fade-in-image.active {
    animation: fade-in 2s;
    border-radius: 10px;
    opacity: 1;
}
@media only screen and (max-width: 1000px) {

  .black_section {
    height: auto;
    width: 100vw;
  }

  .black_section p, .black_section span{
    font-size: 1.2rem;
  }

  .black_section h2{
    line-height: normal;
  }

  .black_section img{
    max-width: 200px;
    padding-top: 20px;
    padding-bottom: 20px;
    margin-top: 50px;
    margin-bottom: 50px;
  }

  .intro {
    height: 40vh;

  }

  .intro h1 {
    font-size: 1.5em;
  }

  .intro h2 {
    font-size: 3em;
    
  }

  .intro h3 {
    font-size: 1.5em;
    margin-top: 3px;
  }

  .line {
    height: 350px;
    z-index: -100;
    opacity: 70%;
  }

  .next_line {
    z-index: -100;
    opacity: 70%;
    position: absolute;
  }

  .info,
  .goal {
    font-size: 1.5em;
    margin: 0;
  }

  .goal{
    margin-bottom: 100px;
  }

  .BusinessCardBack {
    width: fit-content;
  }

  .BusinessCardFront {
    width: fit-content;
  }
}
</style>