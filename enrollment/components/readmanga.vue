<template>
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

</template>