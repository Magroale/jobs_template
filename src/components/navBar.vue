<template>
  <div class="">
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <!-- Container wrapper -->
      <div class="container-fluid">
        <!-- Toggle button -->
        <button class="navbar-toggler" type="button" data-mdb-toggle="collapse" data-mdb-target="#navbarRightAlignExample"
          aria-controls="navbarRightAlignExample" aria-expanded="false" aria-label="Toggle navigation">
          <i class="fas fa-bars"></i>
        </button>

        <!-- Collapsible wrapper -->
        <div class="collapse navbar-collapse" id="navbarRightAlignExample">
          <!-- Left links -->
          <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="#">Empleos</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Bootcamp</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Sobre nostros</a>
            </li>
            <!-- Navbar dropdown -->
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-mdb-toggle="dropdown"
                aria-expanded="false">
                Para profesionales
              </a>
              <!-- Dropdown menu -->
              <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
                <li>
                  <a class="dropdown-item" href="#">Inicio</a>
                </li>
                <li>
                  <a class="dropdown-item" href="#">Empleos</a>
                </li>
                <!-- <li>
                  <hr class="dropdown-divider" />
                </li> -->
                <li>
                  <a class="dropdown-item" href="#">Cursos y Retos</a>
                </li>
                <li>
                  <a class="dropdown-item" href="#">Preguntas</a>
                </li>
                <li>
                  <a class="dropdown-item" href="#">Profesores</a>
                </li>
                <li>
                  <a class="dropdown-item" href="#">Bootcamp</a>
                </li>
              </ul>
            </li>
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-mdb-toggle="dropdown"
                aria-expanded="false">
                Para empresas
              </a>
              <!-- Dropdown menu -->
              <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
                <li>
                  <a class="dropdown-item" href="#">Inicio</a>
                </li>
                <li>
                  <a class="dropdown-item" href="#">Publicar Empleo</a>
                </li>
                <!-- <li>
                  <hr class="dropdown-divider" />
                </li> -->
                <li>
                  <a class="dropdown-item" href="#">Nuestro Proceso</a>
                </li>
                <li>
                  <a class="dropdown-item" href="#">Precios</a>
                </li>
                <li>
                  <a class="dropdown-item" href="#">Pruebas online</a>
                </li>
                <li>
                  <a class="dropdown-item" href="#">Nomina</a>
                </li>
                <li>
                  <a class="dropdown-item" href="#">Blog</a>
                </li>
                <li>
                  <a class="dropdown-item" href="#">Comercial</a>
                </li>
                <li>
                  <a class="dropdown-item" href="#">Calculadora de salario</a>
                </li>
              </ul>

            </li>
            <button type="button" class="btn btn-outline-secondary margin-right m-1" disabled><i class="fas fa-globe margin-right m-1"></i>Español</button>

            <a class="dropdown-toggle d-flex align-items-center hidden-arrow" href="#" id="navbarDropdownMenuAvatar"
              role="button" data-mdb-toggle="dropdown" aria-expanded="false">
              <img src="https://mdbcdn.b-cdn.net/img/new/avatars/2.webp" class="rounded-circle" height="25"
                alt="Black and White Portrait of a Man" loading="lazy" />
            </a>
            <ul class="dropdown-menu dropdown-menu-end" aria-labelledby="navbarDropdownMenuAvatar">
              <li>
                <a class="dropdown-item" href="#">My profile</a>
              </li>
              <li>
                <a class="dropdown-item" href="#">Settings</a>
              </li>
              <li>
                <a class="dropdown-item" href="#">Logout</a>
              </li>
            </ul>
          </ul>
          <!-- Left links -->
        </div>
        <!-- Collapsible wrapper -->
      </div>
      <!-- Container wrapper -->
    </nav>
  </div>
</template>
  
<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {

    }
  },
  methods: {
  },
}
</script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>