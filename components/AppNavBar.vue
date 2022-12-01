<template>
 <div>
  <b-navbar toggleable="lg" type="dark" variant="dark">
    <b-navbar-brand href="#">Enrollment</b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-navbar-nav>
        <tr>
        <th class="nav-item">
          <NuxtLink to="/home" class="nav-link">Home</NuxtLink>
        </th>
        <th class="nav-item">
          <NuxtLink to="/dashboard" class="nav-link">Dashboard</NuxtLink>
        </th>
        <th class="nav-item">
          <NuxtLink to="/enroll" class="nav-link">Enroll Form & List</NuxtLink>
        </th>
      </tr>
      </b-navbar-nav>

      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
        <b-nav-form>
          <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
          <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
        </b-nav-form>

        <b-nav-item-dropdown right>
          <!-- Using 'button-content' slot -->
          <template #button-content>
            <em>User</em>
          </template>
          <b-dropdown-item><NuxtLink to="/login" class="nav-link">Sign Out</NuxtLink></b-dropdown-item>
        </b-nav-item-dropdown>
      </b-navbar-nav>
    
  </b-navbar>
</div>
</template>


