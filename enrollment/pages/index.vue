<template>
  <section class="vh-100" style="background-color: #49D49D;">
  <div class="container py-5 h-100">
    <div class="row d-flex justify-content-center align-items-center h-100">
      <div class="col col-xl-10">
        <div class="card" style="border-radius: 1rem; background-color: #FC9F5B;">
          <div class="row g-0">
            <div class="col-md-6 col-lg-5 d-none d-md-block">
              <img src="https://lh5.googleusercontent.com/WN9okGCwyxV0faaFtEhg7m5crmcaqcXJlY6cI6popzsZ776q7-63uiYoUbz69whYcqrw49sv1pNTjEdV2N0xF9h4D8d2m8-3PwHggAuV1Kyl4UuYGIdORdPUK5TrbMMGXA=w1280"
                alt="login form" class="img-fluid" style="border-radius: 1rem 0 0 1rem;" />
            </div>
            <div class="col-md-6 col-lg-7 d-flex align-items-center">
              <div class="card-body p-4 p-lg-5 text-black">

                <form>

                  <div class="d-flex align-items-center mb-3 pb-1">
                    <i class="fas fa-cubes fa-2x me-3" style="color: #49D49D;"></i>
                    <span class="h1 fw-bold mb-0">HOI SULOD DIRI</span>
                  </div>

                  <h5 class="fw-normal mb-3 pb-3" style="letter-spacing: 1px;">Login dadi bi</h5>

                  <div class="form-outline mb-4">
                    <input type="email" id="form2Example17" class="form-control form-control-lg" />
                    <label class="form-label" for="form2Example17">Imong Email Palihug</label>
                  </div>

                  <div class="form-outline mb-4">
                    <input type="password" id="form2Example27" class="form-control form-control-lg" />
                    <label class="form-label" for="form2Example27">Kabalo naka unsa ni</label>
                  </div>

                  <div class="pt-1 mb-4">
                    <button class="btn btn-dark btn-lg btn-block" type="button">SUD DAYUN</button>
                  </div>

                  <a class="small text-muted" href="#!">Naa kay amnesia?</a>
                  <p class="mb-5 pb-lg-2" style="color: #393f81;">Wala kay account? <a href="#!"
                      style="color: #393f81;">Unsa imo gipaabot? Ali na</a></p>
                  <a href="#!" class="small text-muted">Termino sa paggamit</a>
                  <a href="#!" class="small text-muted">Patakaran sa Pagkapribado</a>
                </form>

              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
</template>

<style>
.img-fluid{
background-size: cover;
width: 100%;
height: 100%;
background-position: center;
}
</style>

<script>
export default {
  name: 'IndexPage',
}
</script>
