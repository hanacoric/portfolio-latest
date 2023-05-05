<template>
     <section class="video_cv_section">
        <h1>// CHECK  MY VIDEO CV! ;) //</h1>
        <a href="https://youtu.be/YgIwut9sDHA">Here is my Video CV</a>
        <h1>// CHECK  MY VIDEO CV! ;) //</h1>
    </section>
</template>

<style>
.video_cv_section{
    height: 50vh;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
    background-color: #D4D4D2;
}

.video_cv_section h1{
    font-family: belfastgroteskbold;
    font-size: 3em;
}

.video_cv_section a{
    text-decoration: none;
    color: black;
    font-size: 2em;
}

@media only screen and (max-width: 1000px) {

    .video_cv_section{
        height: 300px;
        justify-content: space-between;
    }

    .video_cv_section h1{
        font-size: 1.2rem;
        margin-top: 30px;
        margin-bottom: 30px;
    }

    .video_cv_section a{
        font-size: 1rem;
    }
}
</style>