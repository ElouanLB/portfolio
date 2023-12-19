<template>
    <footer>
      <div class="social-icons">
        <a href="https://github.com/ElouanLB" target="_blank" rel="noopener noreferrer">
          <img src="../assets/icons/signe-github.png" alt="GitHub" />
        </a>
        <a href="https://www.linkedin.com/in/elouan-le-bolloch-738b1b295/" target="_blank" rel="noopener noreferrer">
          <img src="../assets/icons/linkedin.png" alt="LinkedIn" />
        </a>
        <a href="https://twitter.com/elouanlbolloch" target="_blank" rel="noopener noreferrer">
          <img src="../assets/icons/twitter.png" alt="Twitter">
        </a>
      </div>
      <div class="last-update">
        <time>Dernière mise à jour : {{ lastUpdateDate }} </time>
      </div>
    </footer>
</template>
  
<script>
export default {
  data() {
    return {
      lastUpdateDate: "01 janvier 2023",
    };
  },
  methods: {
    updateLastUpdateDate() {
      const currentDate = new Date().toLocaleDateString("fr-FR");
      this.lastUpdateDate = currentDate;
    },
  },
  mounted() {
    // Appel de la méthode lors du montage du composant (peut varier en fonction de votre logique)
    this.updateLastUpdateDate();
  },
};
</script>


  
<style scoped>
  footer {
    background-color: lightskyblue;
    color: white;
    padding: 20px 0px;
    text-align: center;
    font-size: 1.1rem;
    width: 1300px;
  }
  
  .social-icons {
    display: flex;
    justify-content: center;
    margin-bottom: 10px;
  }
  
  .social-icons img {
    width: 40px;
  }

  .social-icons a {
    margin: 0 10px;
  }
  
  .last-update {
    font-size: 1rem;
  }
</style>
  