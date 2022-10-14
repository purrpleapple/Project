<template>
  <section class="vh-100" style="background-color: #49D49D;">

  <nav class="navbar navbar-expand-lg navbar-light bg-light" style="background-color: #3590F3;">
    <a class="navbar-brand" href="#">
    <img src="logo.png" width="150" height="50" class="d-inline-block align-top" alt="">
    </a>

  <button class="navbar-toggler" type="button" data-toggle="collapse"  data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
    <div class="navbar-nav">
      <a class="nav-item nav-link active" href="#">Home <span class="sr-only">(current)</span></a>
      <a class="nav-item nav-link" href="#"><NuxtLink to="/dashboard">Dashboard</NuxtLink></a>
      <a class="nav-item nav-link" href="#"><NuxtLink to="/orders">Order</NuxtLink></a>
      <a class="nav-item nav-link" href="#"><NuxtLink to="/products">Products</NuxtLink></a>
      <a class="nav-item nav-link" href="#"><NuxtLink to="/customer">Customer</NuxtLink></a>
    </div>
  </div>
  <form class="form-inline">
    <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
    <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
  </form>
</nav>

  <div class="container py-5 h-100">
    <div class="row d-flex justify-content-center align-items-center h-100">
      <div class="col col-xl-10">
        <div class="card" style="border-radius: 1rem; background-color: #FC9F5B;">
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
                    <button class="btn btn-dark btn-lg btn-block" type="button">GET IN</button>
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
