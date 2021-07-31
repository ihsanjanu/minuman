<template>
  <div class="hero">
    <!--desktop-->
    <div class="d-none d-md-block">
      <div class="row mt-4">
        <div class="col-md-6">
          <img src="../assets/images/hero.png" width="100%" />
        </div>
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <strong>let's have coffe, </strong> <br />make your days
                colorful
              </h2>
              <p>Ayo segera pesan dan bercerita</p>
              <router-link to="/Drink" class="btn btn-lg btn-succes"
                >Order Now</router-link
              >
            </div>
          </div>
        </div>
      </div>
    </div>

    <!--mobile-->
    <div class="d-sm-block d-md-none">
      <div class="row mt-4">
        <div class="col-md-6 mb-3">
          <img src="../assets/images/hero.png" width="100%" />
        </div>
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <strong>let's have coffe, </strong> <br />
                make your days colorful
              </h2>
              <p>Ayo segera pesan dan bercerita</p>
              <router-link to="/Drink" class="btn btn-lg btn-succes"
                >Order Now</router-link
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "hero",
};
</script>

<style>
</style>