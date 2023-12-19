<template>
<section class="container">
    <div>
        <h3>CV</h3>
        <img src="../assets/img/cv.JPG" alt="image du cv">
    </div>
    <div>
        <h3>Dynamiser un espace commentaire</h3>
        <img src="../assets/img/Dynamiser un espace commentaire.JPG" alt="image de la création Dynamiser un espace commentaire">
    </div>
    <div>
        <h3>Cahier des charges</h3>
        <img src="../assets/img/Cahier des charges.JPG" alt="image du cahier des charges">
    </div>
</section>
</template>

<script>
</script>

<style scoped>
.container {
    display: flex;
    justify-content: space-between;
}


h3 {
    display: flex;
    justify-content: center;
}

img {
   display: flex;
   width: 350px;
   padding: 20px;
   height: 500px;
   border: 2px solid lightblue;
}

img:hover {
    transition: 1s;
    box-shadow: 20px 10px 15px lightblue;
}
</style>