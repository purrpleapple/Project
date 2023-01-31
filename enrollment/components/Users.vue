<template>
  <body style="background-color: #49D49D;">
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
      <a class="nav-item nav-link" href="#"><NuxtLink to="/read">Read Manga</NuxtLink></a>
      <a class="nav-item nav-link" href="#"><NuxtLink to="/watch">Watch Anime</NuxtLink></a>
      <a class="nav-item nav-link" href="#"><NuxtLink to="/market">Marketplace</NuxtLink></a>
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
    <div class="form-inline" action="#">
      <input type="text" id="FirstName" v-model="item.firstname" placeholder="First Name" class="form-control">
      <input type="text" id="LastName" v-model="item.lastname" placeholder="Last Name" class="form-control">
      <button @click="addItem" id="AddUser" class="btn btn-dark"><i class="fas fa-plus">Add</i></button>
        </div>
        <table id="UserTable" class="table table-striped table-bordered table-sm" style="color: white; background-color: palevioletred;">
        <thead class="thead-light">
          <th>First Name</th>
          <th>Last Name</th>
          <th class="col-2">Edit/Delete</th>
        </thead>
        <tr v-for="item in items" :key="item.firstname">
          <td>
            <input v-if="item.edit" type="text" v-model="item.firstname">
            <span v-else>{{item.firstname}}</span>
          </td>
          <td>
            <input v-if="item.edit" type="text" v-model="item.lastname">
            <span v-else>{{item.lastname}}</span>
          </td>
          <td><button @click="ItemEdit(item)" class="btn btn-info"><i class="far fa-edit">edit</i></button>
            <button @click="removeItem(item)" class="btn btn-danger"><i class="far fa-trash-alt">delete</i></button></td>
        </tr>
      </table>
  </body>
  
  </template>
  

  <style scoped>
  .form-inline input {
    margin-right:8px;
  }
  </style>

  <script scope>
  let url = "http://localhost:3002/users";
    export default {
      data() {
      return {
        item: {id: 0, firstname: "", lastname: "", edit: false},
        items: [],
        tempData: []
      }
    },
    methods:{
      async addItem() {
        console.log(this.item.id);
        await this.$axios.$post(url + '/insert', this.item)
        .then((res) => {
          console.log(res);
          this.item = {id: "0", firstname: "", lastname: "", edit: false};
        })
        .catch((err) => console.log(err));
        this.GetAllData();
        this.GetCurrentID();
      },
      async removeItem(item){
        await this.$axios.$post(url + '/delete', {id: item.id})
        .then((res) => {
          console.log(res);
          this.GetAllData();
      })
      .catch((err) => console.log(err));
      },
      async GetAllData(){
        this.items = await this.$axios.$get(url)
        .then((res) => {
          console.log(res);
          this.tempData = res;
          console.log(this.items);
        })
        .catch((err) => console.log(err));
        this.items = this.tempData;
        this.GetCurrentID();
      },
      async ItemEdit(item) //For Updating
      {
        if(!item.edit)
        {
          item.edit = !item.edit
        }
        else
        {
          item.edit = !item.edit
          console.log(item);
          await this.$axios.$post(url + '/update', item)
          .then((res) => {
            console.log(res);
          })
          .catch((err) => console.log(err));
        }
      },
      GetCurrentID(){
        this.item.id = Math.max.apply(Math, this.items.map(function(o) { return o.id; })) + 1;
      }
    },
    async mounted(){
      await this.GetAllData();
    }
  }
  </script>
  

  
  