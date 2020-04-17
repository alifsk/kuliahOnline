<template>

    <div id="app">
        <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.2.0/css/all.css" integrity="sha384-hWVjflwFxL6sNzntih27bfxkr27PmbbK/iSvJ+a4+0owXq79v+lsFkW54bOGbiDQ" crossorigin="anonymous">
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/material-design-iconic-font/2.2.0/css/material-design-iconic-font.min.css">
        <link rel="stylesheet" href="path/to/material-design-iconic-font/css/material-design-iconic-font.min.css">
        <div>
            <b-navbar class="navbar" id="nav" toggleable="lg" fixed="top">
                <b-navbar-brand  class="navbar-brand m-auto" href="#home">
                    <img src="./assets/images/logo.png" alt="logo" class="logo">
                </b-navbar-brand>
                <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
                <b-collapse id="nav-collapse" class="nav-collapse" is-nav>
                    <b-navbar-nav class="mr-auto">
                        <b-nav-item class="nav-item" href="/" right><b>Home</b></b-nav-item>
                        <b-nav-item class="nav-item" href="/about" right><b>About Us</b></b-nav-item>
                        <b-nav-item-dropdown class="nav-item" text="Product" right>
                            <b-dropdown-item href="/produk/pod"><b>MOD</b></b-dropdown-item>
                            <b-dropdown-item href="/produk/mod"><b>POD</b></b-dropdown-item>
                            <b-dropdown-item href="/produk/liquid"><b>Liquid</b></b-dropdown-item>
                        </b-nav-item-dropdown>
                        <b-nav-item class="nav-item" href="/contact" right><b>Contact Us</b></b-nav-item>
                        <b-nav-item class="nav-item" href="/login" right><b>Sign In</b></b-nav-item>
                    </b-navbar-nav>
                </b-collapse>
                <b-collapse id="nav-collapse" class="nav-collapse" is-nav>
                    <b-navbar-nav class="ml-auto">
                        <b-nav-item class="nav-item" href="" right>
                            <i class="fas fa-search"></i>
                        </b-nav-item>
                        <b-nav-item class="nav-item" href="" right>
                            <i class="fas fa-user"></i>
                        </b-nav-item>
                        <b-nav-item class="nav-item" href="" right>
                            <i class="fas fa-shopping-cart"></i>
                        </b-nav-item>
                    </b-navbar-nav>
                </b-collapse>
            </b-navbar>
        </div>
        <router-view />
    </div>
</template>

<script>
export default {
  mounted() {
    this.$nextTick(() => {
      window.addEventListener('scroll', () => {
        const navbar = document.getElementById('nav');
        // eslint-disable-next-line camelcase
        const nav_class = navbar.classList;
        if (document.documentElement.scrollTop >= 150) {
          if (nav_class.contains('shrink') === false) {
            nav_class.toggle('shrink');
          }
        } else if (nav_class.contains('shrink') === true) {
          nav_class.toggle('shrink');
        }
      });
    });
  },
};
</script>
<style>

html {
    scroll-behavior: smooth;
}
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: none;
    color: #2c3e50;
    margin-top: 0;
}
.navbar {
    background-color: transparent;
    transition: 0.3s ease;
}
nav.shrink {
    background-color: white;
    box-shadow: 0 1px 4px 0 rgb(0, 0, 0, 5);
}
.nav-item {
    padding-left: 5px;
    padding-right: 5px;
    color: black;
}
.logo {
    width: 140px;
    opacity: 0.5;
    padding: 20px;
}
</style>