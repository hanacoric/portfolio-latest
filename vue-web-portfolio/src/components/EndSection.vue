<template>
     <section class="end_section">
      <div class="pdf_cv_section">
        <div class="start_pdf_button">
          <a href="https://drive.google.com/file/d/1Hxh_n4hGnhjIEN4TqpnR5HMZaad9q7xO/view?usp=sharing" download id="download-pdf-btn">!! CLICK FOR PDF !!</a>
        </div>
        <img src="../assets/images/portfolio-cv.jpg" class="cv_img" alt="pdfcv">
        <div class="end_pdf_button">
          <a href="https://drive.google.com/file/d/1Hxh_n4hGnhjIEN4TqpnR5HMZaad9q7xO/view?usp=sharing" download id="download-pdf-btn">!! CLICK FOR PDF !!</a>
        </div>
      </div>

      <div class="footer_section">
        <h1>GET IN TOUCH</h1>
        <a href="https://accounts.google.com/b/0/AddMailService">hanacoric2@gmail.com</a>
        <a href="https://www.linkedin.com/in/hanacoric1411/">
          <img src="../assets/images/linkedin.png" alt="linkedin">
        </a>
      </div>
    </section>
</template>

<style>
.end_section{
    height: 130vh;
    background-color: white;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
}

.cv_img{
    width: 420px;
    height: 543px;
}

.pdf_cv_section{
    height: max-content;
    display: flex;  
    align-items: center;
    margin-top: 20vh;
}

.start_pdf_button{
    height: 65vh;
    font-family: belfastgroteskbold;
    writing-mode: tb-rl;
    transform: rotate(-180deg);
    display: flex;
    justify-content: flex-end;
    color: #D4D4D2;
    text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
}

.end_pdf_button{
    height: 65vh;
    font-family: belfastgroteskbold;
    writing-mode: vertical-rl;
    display: flex;
    justify-content: flex-end;
    color: #D4D4D2;
    text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
}

.end_pdf_button a, .start_pdf_button a{
    font-family: belfastgroteskbold;
    text-decoration: none;
    color: #D4D4D2;
    text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
    font-size: 2em;
}

.footer_section{
    height: 25vh;
    display: flex;
    justify-content: space-evenly;
    flex-direction: column;
    align-items: center;
}

.footer_section h1{
    display: flex;
    justify-content: space-evenly;
    flex-direction: column;
    align-items: center;
    height: min-content;
}

.footer_section a{
    text-decoration: none;
    color: black;
}

@media only screen and (max-width: 1024px) {
  .end_section {
    height: 100vh;
    width: 100vw;
  }
  .pdf_cv_section {
    flex-direction: row;
    align-items: center;
    margin-top: 10vh;
  }
  .cv_img {
    width: 300px;
    height: 413px;
  }
  .start_pdf_button, .end_pdf_button {
    font-size: 7px;
    height: 400px;
  }
}

</style>