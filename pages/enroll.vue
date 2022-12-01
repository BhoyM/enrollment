<template>
    <div>
    <div class="container">
    <AppNavBar />
    </div>

    <body>
<div class="container-enroll">
    <br>
    <div class="form-inline" action="#">
    <input type="text" id="form-name" v-model="item.name" placeholder="StudentName" class="form-control">
    <input type="text" id="form-Lname" v-model="item.Lname" placeholder="StudentLastName" class="form-control">
    <input type="text" id="form-Add" v-model="item.Add" placeholder="StudentAddress" class="form-control">
    <input type="date" id="form-Dob" v-model="item.Dob" placeholder="DateOfBirth(mm/dd/yy)" class="form-control">
    <input type="text" v-model="item.desc" placeholder="StudentCourse" class="form-control" v-on:keyup.enter="addItem">
    <button @click="addItem" class="btn btn-dark">Add on Item<i class="fas fa-plus"></i></button>
      </div>
    <br><br>
    <table class="table table-striped table-bordered table-sm">
      <thead class="thead-light">
        <th>Student Name</th>
        <th>Student Last Name</th>
        <th>StudentAdd</th>
        <th>DateOfBirth</th>
        <th>Course</th>
        <th class="col-3">Edit/Del</th>
      </thead>
      <tr v-for="item in items" :key="item.name">
        <td>
          <input v-if="item.edit" type="text" v-model="item.name"  v-on:keyup.enter="item.edit = !item.edit">
          <span v-else>{{item.name}} </span>
        </td>
        <td>
          <input v-if="item.edit" type="text" v-model="item.Lname"  v-on:keyup.enter="item.edit = !item.edit">
          <span v-else>{{item.Lname}} </span>
        </td>
        <td>
          <input v-if="item.edit" type="text" v-model="item.Add"  v-on:keyup.enter="item.edit = !item.edit">
          <span v-else>{{item.Add}} </span>
        </td>
        <td>
          <input v-if="item.edit" type="text" v-model="item.Dob"  v-on:keyup.enter="item.edit = !item.edit">
          <span v-else>{{item.Dob}} </span>
        </td>
        <td>
          <input v-if="item.edit" type="text" v-model="item.desc" v-on:keyup.enter="item.edit = !item.edit">
          <span v-else>{{item.desc}} </span>
        </td>
        <td><button @click="item.edit = !item.edit" class="btn btn-info">Edit The Item<i class="far fa-edit"></i></button>
          <button @click="removeItem(index)" class="btn btn-danger">Erase The Item<i class="far fa-trash-alt"></i></button></td>
      </tr>
    </table>
</div>


    </body>

</div>
</template>

<script scope>
  export default {
    data() {
    return {
      item: {name: "", Lname: "", Add: "", Dob: "", desc: "", edit: false},
      items: []
    }
  },
  methods:{
    addItem() {
      this.items.push({
        name:this.item.name,Lname:this.item.Lname, Add:this.item.Add, Dob:this.item.Dob, desc:this.item.desc, edit: false}
        );
      this.item = [];
    },
    removeItem(index){
      this.items.splice(index, 1)
    }
  }
  }
</script>






<style scoped>
.form-inline input {
  margin-right:8px;
}

nav {
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    background-color: #ef3636;
  }

li {
    float: left;
    border-right:1px solid #bbb;
  }

li:last-child {
    border-right: none;
  }

li a {
    display: block;
    color: white;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
  }

li a:hover:not(.active) {
    background-color: #111;
  }
</style>
<style scoped>
nav {
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    background-color:orange;
  }

li {
    float: left;
    border-right:1px solid #bbb;
  }

li:last-child {
    border-right: none;
  }

li a {
    display: block;
    color: white;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
  }

li a:hover:not(.active) {
    background-color: #111;
  }
</style>
