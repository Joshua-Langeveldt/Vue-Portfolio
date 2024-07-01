<template>
    <nav class="navbar navbar-expand-lg fixed-top ">
          <div class="container-fluid">
            <router-link class="navbar-brand" to="/">
              <img
                src="https://joshua-langeveldt.github.io/images/images/Logo/AltLogo.png"
                alt="logo"
                loading="lazy"
              />
            </router-link>
            <button
              class="navbar-toggler"
              type="button"
              data-bs-toggle="offcanvas"
              data-bs-target="#offcanvasNavbar"
              aria-controls="offcanvasNavbar"
              aria-label="Toggle navigation"
            >
              <span class="navbar-toggler-icon"></span>
            </button>
            <div
              class="offcanvas offcanvas-end"
              tabindex="-1"
              id="offcanvasNavbar"
              aria-labelledby="offcanvasNavbarLabel"
            >
              <div class="offcanvas-header">
                <router-link class="navbar-brand" to="/">
                  <a href="#home"></a>
                  <img
                    src="https://joshua-langeveldt.github.io/images/images/Logo/LOGO.png"
                    alt="logo"
                    loading="lazy"
                  />
                </router-link>
                <button
                  type="button"
                  class="btn-close"
                  data-bs-dismiss="offcanvas"
                  aria-label="Close"
                ></button>
              </div>
              <div class="offcanvas-body">
                <ul
                  class="navbar-nav fw-bolder ms-auto"
                >
                  <li class="nav-item">
                    <router-link
                      class="nav-link font-weight-bold"
                      aria-current="page"
                      to="/"
                      >Home</router-link
                    >
                  </li>
                  <li class="nav-item">
                    <a class="nav-link" aria-current="page" href="#about">About</a>
                  </li>
                  <li class="nav-item">
                    <a class="nav-link" aria-current="page" href="#education">Education</a>
                  </li>
                  <li class="nav-item">
                    <a class="nav-link" aria-current="page" href="#skills">Skills</a>
                  </li>
                  <li class="nav-item">
                    <a class="nav-link" aria-current="page" href="#testimonials">Testimonials</a>
                  </li>
                  <li class="nav-item">
                    <a class="nav-link" aria-current="page" href="#projects">Projects</a>
                  </li>
                  <li class="nav-item">
                    <a class="nav-link" aria-current="page" href="#contact">Contact Me</a>
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </nav>
  </template>
  
  <script>
  export default {
      name: "NavComp"
  }
  </script>
  
  <style scoped>
  
  </style>