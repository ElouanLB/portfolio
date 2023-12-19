<template>
    <header>
        <a href="http://localhost:5173/"><img src="../assets/icons/icons/profil.JPG" alt="photo de profil"></a>
        <h1>Elouan Le Bolloch</h1>
        <nav>
           <RouterLink class="link" to="/">Accueil</RouterLink>
           <RouterLink class="link" to="/" @click.prevent="scrollToCreations">Créations</RouterLink>
           <RouterLink class="link" to="/" @click.prevent="scrollToContact">Contact</RouterLink>
           <RouterLink class="link" to="/test404">Test 404</RouterLink>
        </nav>
    </header>
</template>

<script>
export default {
  methods: {
    scrollToCreations() {
      this.scrollToElement('creations');
    },
    scrollToContact() {
      this.scrollToElement('contact');
    },
    scrollToElement(elementId) {
      const targetElement = document.getElementById(elementId);

      if (targetElement) {
        const offsetTop = targetElement.offsetTop;

        window.scrollTo({
          top: offsetTop,
          behavior: 'smooth',
        });
      }
    },
  },
};
</script>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@400;500;700&display=swap');

  * {
    font-family: "Quicksand",sans-serif;
    justify-content: center;
  }

header {
    display: flex;
    width: 1300px;
    flex-direction: column;
    margin: auto;
    align-items: center;
    text-align: center;
    background-image: url(../assets/img/360_F_318606217_Hk8jo2MVoI33SQOkYrfOF929J7JgIP0P.jpg);
    background-size: cover;
    background-position: center;
    justify-content: center;
    border-radius: 0px 0px 10px 10px;
}

h1 {
    color: white;
}

img{
    height: 150px;
    width: 150px;
    border-radius: 100px;
    box-shadow:  0px 0px 10px lightskyblue, 0px 0px 10px lightskyblue;
    object-fit: cover;
}

img:hover {
    cursor:grab;
}


nav{
  display: flex;
    width: 100%;
    justify-content: space-between;
    padding: 20px 0px 20px 0px;
    text-align: center;
    background-color: lightskyblue;
    box-shadow: 0px 0px 20px lightskyblue ;
    border-radius: 10px;
}
.link {
    display: flex;
    padding: 0px 70px;
    font-size: 1.2rem;
    font-weight: 600;
    -webkit-transition: color 1s;
    transition: color 1s;
}

.link:hover{
    color:black;
}

a {
    color: white;
    text-decoration: none;
}
</style>