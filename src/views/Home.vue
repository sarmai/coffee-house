<template>
  <div>
    <div class="container">
      <h1 class="title">
        <span>GG</span><span>Co</span><span>ff</span><span>ee</span>
      </h1>
      <img
        class="img"
        src="../assets/img/entrance.jpg"
        alt="Coffee shop entrance"
      />
    </div>
    <div class="info">
      <h3 class="info-title">ALL DAY CAFÉ</h3>
      <div class="info-body">
        <p>Patio + dining room open 7 days a week.</p>
        <p>Takeaway available daily.</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  position: relative;
  height: 100vh;
}

.img {
  background-color: var(--secondary-dark);
}

.title {
  display: grid;
  grid-template-rows: repeat(4, 150px);
  grid-template-columns: repeat(4, minmax(100px, 1fr));
  margin: 0;
  position: absolute;
  z-index: 99;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: white;
  text-transform: uppercase;
  font-size: 7rem;
  font-family: "Bodoni Moda", serif;
}

.title span:nth-child(1) {
  grid-row: 3/4;
  grid-column: 1/2;
}

.title span:nth-child(2) {
  grid-row: 1/2;
  grid-column: 2/3;
}

.title span:nth-child(3) {
  grid-row: 2/3;
  grid-column: 3/4;
}

.title span:nth-child(4) {
  grid-row: 4/5;
  grid-column: 4/5;
}

.info {
  padding: 1em 3em;
}

.info-title {
  text-transform: uppercase;
  letter-spacing: 0.2em;
  color: var(--primary-dark);
}

.info-body {
  margin: 2em 0;
}

@media (max-width: 900px) {
  .container {
    height: 60vh;
  }
  .title {
    font-size: 5rem;
    grid-template-rows: repeat(4, 80px);
  }
}
</style>
