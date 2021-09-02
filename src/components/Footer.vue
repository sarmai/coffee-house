<template>
  <div class="nav-footer">
    <label class="nav-form-title" for="mailingList">Mailing List</label>
    <form class="nav-form" id="mailingList">
      <input type="email" name="Email" placeholder="EMAIL" id="email" />
      <input type="button" value="I love coffee" />
    </form>
    <div class="social-btns">
      <a href=""><i class="fab fa-twitter"></i></a>
      <a href=""><i class="fab fa-instagram"></i></a>
      <a href=""><i class="fab fa-facebook"></i></a>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.nav-form-title {
  color: white;
  text-transform: uppercase;
}

.nav-form {
  margin: 1em 0;
  text-transform: uppercase;
}

.nav-form input {
  font-family: inherit;
  padding: 1em;
  margin: 0.3em 0;
}

.nav-form input[type="email"] {
  width: 100%;
  border: 2px solid white;
}

.nav-form input[type="button"] {
  text-transform: uppercase;
  background-color: unset;
  border: 2px solid white;
  color: white;
  font-weight: 600;
  cursor: pointer;
}

.nav-form input[type="button"]:hover {
  background-color: white;
  color: var(--primary);
}

.social-btns {
  display: flex;
  gap: 1em;
}

.social-btns a {
  color: white;
  font-size: 2rem;
}
</style>
