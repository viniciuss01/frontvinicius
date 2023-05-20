<template>
    <header class="header">
      <img src="@/assets/acme.jpg" alt="ACME" class="header-logo">
    </header>
    <Slide >
      <router-link to="/">
        <span>Início</span>
      </router-link>        
      <router-link to="/alunos">
        <span>Alunos</span>
      </router-link> 
      <router-link to="/cursos">
        <span>Cursos</span>
      </router-link> 
      <router-link to="/matriculas">
        <span>Matrículas</span>
      </router-link> 
    </Slide>    
    <router-view /> 
    <footer class="footer">
      <p>SENAC. &copy; 2023 Todos os direitos reservados.</p>
    </footer>   
  </template>
  
  <script>
  import { Slide } from 'vue3-burger-menu'
  
  export default {
    components: {
      Slide
    },
    methods: {
      closeMenu() { 
        console.log('aqui')       
        this.$refs.slide.toggle() // fecha o menu
      }
    }
  }
  </script>
  

<style>
.header {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 50px;
  background-color: #000000;
  margin-top: 80px;
}

.header-logo {
  width: 100px;
  height: auto;
  object-fit: contain;
}

.footer {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 50px;
  background-color: #f0f0f0;
}

.bm-burger-button {
    position: flex;
    width: 36px;
    height: 30px;
    left: 36px;
    top: 36px;
    cursor: pointer;
}
.bm-burger-bars {
    background-color: #000000;
}
.line-style {
    position: absolute;
    height: 20%;
    left: 0;
    right: 0;
}
.cross-style {
    position: absolute;
    top: 12px;
    right: 2px;
    cursor: pointer;
}
.bm-cross {
    background: #bdc3c7;
}
.bm-cross-button {
    height: 24px;
    width: 24px;
}
.bm-menu {
    height: 100%; /* 100% Full-height */
    width: 0; /* 0 width - change this with JavaScript */
    position: fixed; /* Stay in place */
    z-index: 1000; /* Stay on top */
    top: 0;
    left: 0;
    background-color: rgb(0, 0, 0); /* Black*/
    overflow-x: hidden; /* Disable horizontal scroll */
    padding-top: 60px; /* Place content 60px from the top */
    transition: 0.5s; /*0.5 second transition effect to slide in the sidenav*/
}

.bm-overlay {
    background: rgba(254, 254, 254, 0.3);
}
.bm-item-list {
    color: #b8b7ad;
    margin-left: 10%;
    font-size: 20px;
}
.bm-item-list > * {
    display: flex;
    text-decoration: none;
    padding: 0.7em;
}
.bm-item-list > * > span {
    margin-left: 10px;
    font-weight: 700;
    color: white;
}
</style>
