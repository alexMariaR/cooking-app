<template>
    <footer class="rodape paragrafo">
      Dev  <a href="https://github.com/alexMariaR"> @alexM </a> | 2024 - Vue.js Project
    </footer>
  </template>
  
  <style scoped>
  .rodape {
    background: var(--verde-escuro, #263A29);
    padding: 1.5rem 7.5rem;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  a:-webkit-any-link {
    color: white;
    cursor: pointer;
    text-decoration: underline;
}
  @media only screen and (max-width: 1300px) {
    .rodape {
      padding: 1.5rem 3.75rem;
    }
  }
  
  @media only screen and (max-width: 767px) {
    .rodape {
      padding: 1.5rem;
    }
  }
  </style>