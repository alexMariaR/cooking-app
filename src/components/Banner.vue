

<template>
    <header class="banner">
      <div class="apresentacao">
        <img src="../assets/imagens/logo.svg" alt="Logo Cookin" class="logo">
  
        <p class="cabecalho-lg frase-cabecalho">
          <span class="texto-verde">A feast of ideas to awaken the creative chef in you!</span>
        </p>
  
        <p class="subtitulo-lg">
            Explore new recipes every day with the ingredients that are within your reach!
        </p>
      </div>
  
      <img src="../assets/imagens/foto-banner.png" alt="" class="foto-banner">
    </header>
  
  </template>
  
  <style scoped>
  .banner {
    padding: 4rem 7.5rem;
    color: var(--creme);
  
    display: flex;
    justify-content: space-between;
    align-items: center;
    column-gap: 3.25rem;
  }
  
  .logo {
    height: 4.5rem;
    margin-bottom: 3rem;
  }
  
  .frase-cabecalho {
    margin-bottom: 2rem;
  }
  
  .texto-verde {
    color: var(--verde-medio, #3D6D4A);
  }
  
  .foto-banner {
    width: 35rem;
  }
  
  @media only screen and (max-width: 1300px) {
    .banner {
      padding: 4rem 3.75rem;
      flex-direction: column;
      align-items: center;
      gap: 1rem;
    }
  
    .logo {
      display: block;
      margin-left: auto;
      margin-right: auto;
    }
  }
  
  @media only screen and (max-width: 767px) {
    .banner {
      padding: 4rem 1.5rem;
    }
  
    .foto-banner {
      width: min(100%, 21.25rem);
    }
  }
  
  </style>