<template>
  <section
    id="newsletter"
    class="text-center d-flex flex-column justify-content-center"
  >
    <h3 class="mb-5">Subscribe to our Newsletter</h3>
    <div id="email-input" class="d-flex justify-content-center gap-3">
      <input
        type="text"
        class="form-control"
        placeholder="Insert your email*"
      />
      <button type="button" class="btn btn-dark">SEND</button>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppNewsletter",
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/variables.scss";
#newsletter {
  background-color: $silver-chalice;
  padding: 50px 0;
  input {
    width: 400px;
  }
  button {
    background-color: black;
    width: 200px;
  }
}
</style>