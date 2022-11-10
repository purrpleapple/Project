<template>
    <section class="vh-100" style="background-color: #49D49D;">
        <nav class="navbar navbar-expand-lg navbar-light" style="background-color: #27213C; box-shadow: 5px 5px 5px rgb(0 0 0 / 30%);">
    <a class="navbar-brand" href="#">
    <a href = "http://localhost:51633/"><img src="logo.png" width="130" height="40" class="d-inline-block align-top" alt=""></a>
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
export default 
{
  name: 'marketPlace',
}
</script>