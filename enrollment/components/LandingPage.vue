<template>
  <section class="vh-100" style="background-color: #49D49D;">

  <nav class="navbar navbar-expand-lg navbar-light" style="background-color: #27213C; box-shadow: 5px 5px 5px rgb(0 0 0 / 30%);">
    <a class="navbar-brand" href="#">
    <img src="logo.png" width="130" height="40" class="d-inline-block align-top" alt="">
    </a>

  <button class="navbar-toggler" type="button" data-toggle="collapse"  data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
    <b-dropdown id="dropdown-1" text="Browse" variant="link" toggle-class="text-decoration-none" no-caret class="m-2" aria-hidden="true" style="font-weight: bold; background-color: #27213C ; ">
    <b-dropdown-item href="#">Popular</b-dropdown-item>
    <b-dropdown-item href="#">New</b-dropdown-item>
    <b-dropdown-item href="#">Alphabetical</b-dropdown-item>
    <b-dropdown-item href="#">Seasonal</b-dropdown-item>
    <b-dropdown-item href="#">Release Calendar</b-dropdown-item>
    </b-dropdown>
      <a class="nav-item nav-link" href="#"><NuxtLink to="/readmanga">Read Manga</NuxtLink></a>
      <a class="nav-item nav-link" href="#"><NuxtLink to="/watchanime">Watch Anime</NuxtLink></a>
      <a class="nav-item nav-link" href="#"><NuxtLink to="/marketplace">Marketplace</NuxtLink></a>
      <b-dropdown id="dropdown-2" text="News" variant="link" toggle-class="text-decoration-none" no-caret class="m-2" aria-hidden="true" style="font-weight: bold; background-color: #27213C ; ">
      <b-dropdown-item href="#">All News</b-dropdown-item>
      <b-dropdown-item href="#">Anime Awards</b-dropdown-item>
      <b-dropdown-item href="#">WatchaRead Expo</b-dropdown-item>
      <b-dropdown-item href="#">Anime Movie Night</b-dropdown-item>
      </b-dropdown>
      </div>
  <form class="form-inline">
    <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
    <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
  </form>
</nav>
  <div class="container py-5 h-100">
    <div class="row d-flex justify-content-center align-items-center h-100">
      <div class="col col-xl-10">
        <div class="card" style="border-radius: 1rem; background-color: #FC9F5B; box-shadow: 5px 5px 5px rgb(0 0 0 / 30%);">
          <div class="row g-0">
            <div class="col-md-6 col-lg-5 d-none d-md-block">
              <img src="minilogo.png"
                alt="login form" class="img-fluid" style="border-radius: 1rem 0 0 1rem;" />
            </div>
            <div class="col-md-6 col-lg-7 d-flex align-items-center">
              <div class="card-body p-4 p-lg-5 text-black">

                <form>

                  <div class="d-flex align-items-center mb-3 pb-1">
                    <i class="fas fa-cubes fa-2x me-3" style="color: #49D49D;"></i>
                    <span class="h1 fw-bold mb-0">LOGIN</span>
                  </div>

                  <h5 class="fw-normal mb-3 pb-3" style="letter-spacing: 1px;">Please login your account here!</h5>

                  <div class="form-outline mb-4">
                    <input type="email" id="form2Example17" class="form-control form-control-lg" />
                    <label class="form-label" for="form2Example17">Email Address</label>
                  </div>

                  <div class="form-outline mb-4">
                    <input type="password" id="form2Example27" class="form-control form-control-lg" />
                    <label class="form-label" for="form2Example27">Password</label>
                  </div>

                  <div class="pt-1 mb-4">
                    <b-button class="btn btn-dark btn-lg btn-block" href="#" type="button"><NuxtLink to="/homepage">GET IN</NuxtLink></b-button>
                   
                  </div>

                  <a class="small text-muted" href="#!">Forgot Password?</a>
                  <p class="mb-5 pb-lg-2" style="color: #393f81;">No Account?<a href="#!"
                      style="color: #393f81;">Register now!</a></p>
                  <a href="#!" class="small text-muted">Terms of Use.</a>
                  <a href="#!" class="small text-muted">Private Policy</a>
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
