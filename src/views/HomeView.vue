<template>
<main ref="homeView">
    <h2>Présentation</h2>
  <div class="introduce">
    <p>Bonjour à tous, <br> Je m'appelle Elouan Le Bolloch, j'ai 21 ans et je suis passionné par le monde du développement web. Actuellement en formation au métier de développeur web au Centre Européen de Formation, je m'investis pleinement dans l'acquisition des compétences nécessaires pour exceller dans ce domaine en constante évolution.</p>
    <p >En dehors de ma passion pour le développement, je nourris un amour indéfectible pour le football et le tennis, deux disciplines qui m'ont enseigné la persévérance, l'esprit d'équipe et le goût du challenge. Ces qualités, je les transpose avec enthousiasme dans mon parcours de développeur web, où la collaboration et la résolution de problèmes sont des éléments clés.
    Au-delà du code, j'aime également m'évader avec mes amis, explorer de nouvelles expériences, et parfois me plonger dans l'univers des jeux vidéo, une source d'inspiration infinie pour ma créativité.</p>
  </div>
    <h2 id="creations">Créations</h2>
  
  <section class="creation_modale">
    <div>
      <!-- Appel du composant modale pour chaque modale, ne pas oublier d'appeler le 'setup' (toogleModal, modalActive) -->
      <Modal @close="toggleModal1" :modalActive="modalActive1">
          <div class="modal-content">
            <h4 class="modal-title">CV</h4>
            <p>Date de création le 16/10/2023</p>
            <p>Technologies utilisées : HTML et CSS</p>
            <a href="http://127.0.0.1:5500/src/assets/creations/projet-cv/index.html" target="_blank"><p>Visiter le projet !</p></a>
            <a href="https://github.com/ElouanLB/projet-cv"><p>Lien GitHub !</p></a>
          </div>
        </Modal>
      <h3>CV</h3>
      <img class="creation-image" src="../assets/img/cv.JPG" alt="image de cv" @click="toggleModal1">
    </div>
    <div>
      <Modal @close="toggleModal2" :modalActive="modalActive2">
          <div class="modal-content">
            <h4 class="modal-title">Dynamiser un espace commentaire</h4>
            <p>Date de création : 24/11/2023</p>
            <p>Technologies utilisées : Javascript</p>
            <a href="http://127.0.0.1:5500/src/assets/creations/Dynamiser%20un%20espace%20commentaire/index.html" target="_blank"><p>Visiter le projet !</p></a>
            <a href="https://github.com/ElouanLB/Dynamiser-un-espace-commentaire"><p>Lien GitHub !</p></a>
          </div>
        </Modal>
      <h3>Dynamiser un espace commentaire</h3>
      <img class="creation-image" src="../assets/img/Dynamiser un espace commentaire.JPG" alt="image de commentaire" @click="toggleModal2">
    </div>
    <div>
      <Modal @close="toggleModal3" :modalActive="modalActive3">
          <div class="modal-content">
            <h4 class="modal-title">Cahier des charges</h4>
            <p>Date de création le 29/10/2023</p>
            <p>Technologies utilisées : Open Office</p>
            <a href="https://drive.google.com/file/d/1EuI44qdvKfKr4L9TLmwpkVqrvnC9hQKc/view?usp=drive_link" target="_blank"><p>Visiter le projet !</p></a>
            
          </div>
        </Modal>
        <h3>Cahier des charges</h3>
      <img class="creation-image" src="../assets/img/Cahier des charges.JPG" @click="toggleModal3">
    </div>
  </section>
  <section id="contact">
    <ContactForm />
  </section>
</main>
</template>

<script>
import Modal from "@/components/Modal.vue";
import Creation from '../components/Creation.vue';
import ContactForm from "@/components/ContactForm.vue";
import { ref } from "vue";

export default {
  name: "Home",
  components: {
    Modal,
    ContactForm,
    Creation,
    },
  setup() {
    //Modale 1
    const modalActive1 = ref(false);

    const toggleModal1 = () => {
      modalActive1.value = !modalActive1.value;
    };

    //Modale 2

    const modalActive2 = ref(false);

    const toggleModal2 = () => {
      modalActive2.value = !modalActive2.value;
    };

    //Modale 3
  
    const modalActive3 = ref(false);

    const toggleModal3 = () => {
      modalActive3.value = !modalActive3.value;
    };

    return { 
      modalActive1, 
      toggleModal1,
      modalActive2,
      toggleModal2,
      modalActive3,
      toggleModal3,
    };

  },
};
</script>



<style scoped>

main {
  color: white;
  width: 1300px;
}

h2 {
  -webkit-transition: color 1s;
  transition: color 2s;
  text-align: center;
  padding-top: 50px;
}

h2:hover {
  color:lightskyblue;
}

.introduce {
  display: flex;
  padding: 100px 0px;
  width: 100%;
  justify-items: center;
}
.introduce p {
  display: flex;
  text-align: left;
  padding: 15px 120px;
}

.creations {
  display: flex;
}

.modal-title {
  color: black;
  
}

.creation_modale {
  display: flex;
    justify-content: space-around;
}

.modal-content {
  color: black;
}

.modal-title {
  display: flex;
  justify-content: center;
  font-size: 1.6rem;
}

h3 {
  display: flex;
  justify-content: center;
}

img {
   display: flex;
   width: 300px;
   padding: 20px;
   height: 450px;
   border: 2px solid lightblue;
}

img:hover {
    transition: 1s;
    box-shadow: 20px 10px 15px black;
    cursor: pointer;
}
</style>
