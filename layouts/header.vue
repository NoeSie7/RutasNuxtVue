<template>
  <div class="cols">
    <!-- <nav class="navbar navbar-dark bg-dark">
       <a class="navbar-brand" href="#">Navbar</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
          <div class="navbar-nav">
            <a class="nav-item nav-link active" href="/">Home <span class="sr-only">(current)</span></a>
            <a class="nav-item nav-link" href="#">Features</a>
            <a class="nav-item nav-link" href="#">Pricing</a>
            <a class="nav-item nav-link disabled" href="#">Disabled</a>
          </div>
        </div>
    </nav> -->
    <b-navbar type="dark" variant="primary" toggleable>
    <b-navbar-toggle target="nav_dropdown_collapse"></b-navbar-toggle>
    <b-collapse is-nav id="nav_dropdown_collapse">
      <b-navbar-nav>
        <nuxt-link class="nav-item nav-link" :to="`${basehref}/`">Home</nuxt-link>
        <nuxt-link class="nav-item nav-link" :to="`${basehref}/link`">Link</nuxt-link>
        <!-- Navbar dropdowns -->
        <b-nav-item-dropdown text="User" right>
           <nuxt-link class="dropdown-item" :to="`${basehref}/User/info`">Info</nuxt-link>
           <nuxt-link class="dropdown-item" :to="`${basehref}/User/settings`">Settings</nuxt-link>
        </b-nav-item-dropdown>
        <b-nav-item-dropdown text="RouteParam" right>
            <nuxt-link class="dropdown-item" :to="`${basehref}/User/1`"><span class="m-2" >OP1</span></nuxt-link>
             <nuxt-link class="dropdown-item" :to="`${basehref}/User/2`"> <span class="m-2" >OP2</span></nuxt-link>

        </b-nav-item-dropdown>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
    <nuxt/>
  </div>
</template>
<script>
import env from "../assets/env";
console.log(env);

export default {
  data(){
    return{
      basehref: env[process.env.NODE_ENV].basehref
    }
  }
}
</script>
<style>

</style>
