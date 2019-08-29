<template>
  <div id="app">
    <!-- navbar -->
    <nav class='navbar navbar-expand-sm navbar-dark bg-dark'>
      <div class="navbar-brand">Lab 1 Project</div>
      <ul class="navbar-nav">
        <li class='nav-item'>
          <router-link class='nav-link' to="/">Home</router-link>
        </li>
        <li class='nav-item'>
          <router-link class='nav-link' to="/about">About</router-link>
        </li>
        <li class='nav-item'>
          <router-link class='nav-link' to="/dice">Dice</router-link>
        </li>
        <li class='nav-item'>
          <router-link class='nav-link' to="/faq">FAQ</router-link>
        </li>
        <li class='nav-item'>
          <router-link class='nav-link' to="/calc">Calculator</router-link>
        </li>
        <li class='nav-item'>
          <router-link class='nav-link' to="/clock">Clock</router-link>
        </li>
        <li class='nav-item'>
          <router-link class='nav-link' to="/count">Counters</router-link>
        </li>
      </ul>
    </nav>
    <!-- header -->
    <div class="jumbotron jumbotron-fluid">
      <div class="container">
        <div class="row">
          <div class="col">
              <h1 class='display-3'>Welcome to the Jungle</h1>
              <h5 class='lead'>This is my first Vue app with Bootstrap</h5>
          </div>
        </div>
      </div>
    </div>
    <!-- main content -->
    <div class="container">
      <router-view/>
    </div>
    <!-- footer -->
      <footer class='fixed-bottom bg-dark'>
        <p class="text-white text-center">This is just a simple footer</p>
    </footer>
  </div>
</template>

<style>
</style>
