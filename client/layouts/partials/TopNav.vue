<template>
    <div>
  <b-navbar type="light" variant="light">
      <div class="container">
            <nuxt-link class="navbar-brand" to="/">Jwt-Auth</nuxt-link>
    <b-navbar-toggle target="nav_dropdown_collapse"></b-navbar-toggle>
    <b-collapse is-nav id="nav_dropdown_collapse">
        <b-navbar-nav>
            <li>
                <nuxt-link class="nav-link" to="/dashboard">Dashboard</nuxt-link>

            </li>
        </b-navbar-nav>
        <b-navbar-nav class="ml-auto">
            <li>
                <nuxt-link class="nav-link" to="/dashboard">Login</nuxt-link>
            </li>
            <li>
                <nuxt-link class="nav-link" to="/auth/register">Register</nuxt-link>
            </li>
        </b-navbar-nav>
    </b-collapse>    
    </div>
      
  </b-navbar>
</div>
</template>
