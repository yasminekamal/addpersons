
<template>

<table class="table">
  <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">Name</th>
      <th scope="col">City</th>
    </tr>
  </thead>
  <tbody>
    <tr v-for="person in persons" :key="person.id">
      <td>{{person.id}}</td>
      <td>{{person.name}}</td>
      <td>{{person.city}}</td>
    </tr>
   
  </tbody>
</table>
<h2 class="text-center">Add Person</h2>
  <div class="mb-3">
    <label for="name" class="form-label">Name</label>
    <input type="text" class="form-control" id="name" v-model="name" >
  </div>
  <div class="mb-3">
    <label for="city" class="form-label">City</label>
    <input type="text" class="form-control" id="city" v-model="city">
  </div>
  <button type="button" class="btn btn-primary" @click="addperson">Add</button>
</template>


<script>
import persons from "../persons";
export default {
  data: () => ({
    persons: persons,
    name:'',
    city:''
  }),
  methods: {
      addperson(){
          let p={ }
          let lastid=persons[persons.length-1].id;
          p["id"]=++lastid;
          p["name"]=this.name;
          p["city"]=this.city;
          
          this.persons.push(p);
      }
  },
};
</script>
