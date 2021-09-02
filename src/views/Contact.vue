<template>
  <div class="container">
    <div class="caption">
      <div class="section">
        <h3 class="title">Located</h3>
        <div class="body">
          <p>
            at South Congress Hotel<br />3216 South Congress Ave<br />
            Austin, Texas 78704
          </p>
          <span
            >Validated self parking is available for two hours dependent on
            capacity.</span
          >
        </div>
      </div>
      <div class="section">
        <h3 class="title">Contact</h3>
        <div class="body">
          <p>
            <a href="tel:">+1 (417) 598-8182</a>
          </p>
          <p>
            <a href="mailto:">info@ggcoffee.com</a>
          </p>
        </div>
      </div>
      <div class="section">
        <h3 class="title">Hours</h3>
        <div class="body">
          <p>
            Patio + Dining Room open 7 days a week.<br />Available to-go every
            day.
          </p>
          <div class="frame">
            <p>Sunday-Thursday 7am-8pm</p>
            <p>Friday & Saturday 7am-9pm</p>
          </div>
          <p class="specials">
            <span>Reverse Happy Hour</span> | $2 off beer, wine & menu
            cocktails, Mon-Fri 6pm-8pm
          </p>
        </div>
      </div>
    </div>
    <div class="img-col">
      <img
        src="../assets/img/barista.jpg"
        alt="Barista at the coffee shop making coffee"
        class="img"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "Contact",
};
</script>

<style scoped>
.container {
  position: relative;
  height: 100vh;
  display: grid;
  grid-template: 1fr / repeat(auto-fit, minmax(300px, 1fr));
}

.img-col {
  height: 30vh;
}

.img {
  background-color: var(--secondary-dark);
}

.caption {
  padding: 3em;
  align-self: center;
}

.section {
  margin-bottom: 3em;
  display: grid;
  grid-template: 1fr/ 30px 1fr;
}

.section:last-child {
  margin-bottom: 0;
}

.title {
  grid-column: 1/2;
  grid-row: 1/-1;
  writing-mode: vertical-rl;
  color: var(--primary-dark);
  text-transform: uppercase;
  letter-spacing: 0.1em;
}

.body {
  grid-column: 2/-1;
  grid-row: 1/-1;
  line-height: 2em;
}

.body p {
  margin: 0;
  padding: 0;
}

.body a {
  text-decoration: none;
  color: var(--secondary);
  font-weight: 500;
}

.body span {
  font-style: italic;
  color: var(--primary);
}

.body .frame {
  display: inline-block;
  margin: 1em 0;
  padding: 1em 2em;
  border: 1px solid var(--primary);
}

.specials span {
  font-weight: 500;
  font-style: normal;
}

@media (min-width: 600px) {
  .img-col {
    padding-right: 4em;
    height: 100%;
  }
}
</style>
