<script>
export default {

}
</script>

<template>
  <div class="test404">
    <img src="../assets/img/404-page-not-found-illustration-2048x998-yjzeuy4v.png" alt="">
    <p>404 Not found. La page que vous essayez de trouver n'existe pas.</p>
  </div>
  <div class="goback">
    <p>Revenez en arrière en cliquant <a href="http://localhost:5173">ICI</a></p>
  </div>
</template>



<style scoped>
.test404{
  display: flex;
  justify-content: center;
  font-size: 2rem;
  padding-top: 100px;
  height: 500px;
}
.test404 img{
  width: 250px;
  height: 150px;
}
.test404 p {
  font-size: 2rem;
  color: white;
}

.goback {
  display: flex;
  justify-content: center;
  color: white;
}

.goback a {
  color: white;
}
</style>