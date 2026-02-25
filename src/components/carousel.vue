<template>
  <div class="c" id="carousel">
    <div id="carouselExampleAutoplaying" class="carousel slide" data-bs-ride="carousel">
      <div class="carousel-inner">
        <div class="carousel-item active">
          <img src="../assets/img1.jpg" class="d-block w-100" alt="img1">
        </div>
        <div class="carousel-item">
          <img src="../assets/img2.jpg" class="d-block w-100" alt="img2">
        </div>
        <div class="carousel-item">
          <img src="../assets/img3.jpg" class="d-block w-100" alt="img3">
        </div>
      </div>
      <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleAutoplaying"
        data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
      </button>
      <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleAutoplaying"
        data-bs-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>
    </div>
    <hr>
  </div>

</template>

<style>
.c {
  margin-top: 70px;
  padding: 10px 50px;
}

.carousel-item img {
  height: 500px;
  object-fit: cover;
}

@media (max-width:700px) {
  .c {
    margin-top: 70px;
    padding: 10px 20px;
  }
}
</style>