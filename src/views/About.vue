<template>
  <div>
    <div class="container">
      <div class="img-container">
        <img
          class="img"
          src="../assets/img/pastries.jpg"
          alt="Coffee shop - view from the street"
        />
      </div>
      <div class="caption">
        <h1 class="title">About</h1>
        <i class="fas fa-mug-hot"></i>
        <div class="body">
          <p>
            GG Coffee is a sunny all day café featuring brunch, happy hour and
            dinner.
          </p>
          <p>
            Whether you’re on the way to the office, dashing between meetings or
            looking to sit down and unwind, allow us to be your companion to
            seizing the day.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "About",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  display: grid;
  grid-template: 1fr / repeat(auto-fit, minmax(450px, 1fr));
  min-width: 0;
  height: 88vh;
}

.img-container {
  height: 60vh;
}

.img {
  background-color: var(--primary);
}

.caption {
  padding: 1em;
  align-self: center;
}

.caption .title {
  text-transform: uppercase;
  letter-spacing: 0.2em;
  color: var(--primary-dark);
}

.caption .body {
  line-height: 2.25em;
}

@media (min-width: 900px) {
  .container,
  .img-container {
    height: 100vh;
  }

  .caption {
    padding: 3em;
    width: 90%;
  }
}
</style>
