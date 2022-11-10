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
    <div id="app">
      <div class="container">
        <br>
        <div class="form-inline" action="#">
        <input id="form-name" v-model="item.fname" type="text" placeholder="Date" class="form-control">
        <input id="form-name" v-model="item.lname" type="text" placeholder="Anime Name" class="form-control"> 
        <input v-model="item.cnum" type="text" placeholder="Genre" class="form-control" v-on:keyup.enter="addItem">
        <button @click="addItem" class="btn btn-dark"><i class="fas fa-plus">Add to Favorite List</i></button>
          </div>
        <br><br>
        <table class="table table-striped table-bordered table-sm, text-center" >
          <thead class="thead-light">
            <th>Date Listed</th>
            <th>Anime Name</th>
            <th>Genre</th>
            <th class="col-2">Modify User</th>
          </thead>
          <tr v-for="(item, index) in items" :key="item">
            <td>
              <input v-if="item.edit" v-model="item.fname"  type="text" v-on:keyup.enter="item.edit = !item.edit">
              <span v-else>{{item.fname}} </span>
            </td>
            <td>
              <input v-if="item.edit" v-model="item.lname" type="text" v-on:keyup.enter="item.edit = !item.edit">
              <span v-else>{{item.lname}} </span>
            </td>
            <td>
              <input v-if="item.edit" v-model="item.cnum" type="text" v-on:keyup.enter="item.edit = !item.edit">
              <span v-else>{{item.cnum}} </span>
            </td>
            <td><button @click="item.edit = !item.edit" class="btn btn-info"><i class="far fa-edit">EDIT</i></button>
              <button @click="removeItem(index)" class="btn btn-danger"><i class="far fa-trash-alt">REMOVE</i></button></td>
          </tr>
        </table>
      </div>
    </div>
</section>
    </template>
    
    <script>
    export default {
        name: 'homepage',
        data() {
        return {
          item: {fname: "", lname: "", cnum: "", edit: false},
          items: []
        }
      },
      methods:{
        addItem() {
          this.items.push({
            fname:this.item.fname, lname:this.item.lname, cnum:this.item.cnum, edit: false}
            );
          this.item = [];
        },
        removeItem(index){
          this.items.splice(index, 1)
        }
      }
    }
    </script>
    
    <style>
        .form-inline input {
            margin-right:8px;
        }
    
        .thead-light {
          text-align: center;
        }
    </style>