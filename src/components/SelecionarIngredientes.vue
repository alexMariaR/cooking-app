<script lang="ts">
import { obterCategorias } from '@/http/index';
import type ICategoria from '@/interfaces/ICategoria';
import CardCategoria from './CardCategoria.vue';
import BotaoPrincipal from './BotaoPrincipal.vue';

export default { 
    data(vm) {
        return{
            categorias: [] as ICategoria[]//propriedade reativa
        };
    },
   
async created() { 
this.categorias = await obterCategorias();
    },
    components: { CardCategoria , BotaoPrincipal}
}
</script>

<template>
   <section class="selecionar-ingredients">
    <h1 class="cabecalho titulo-ingredientes">
        Ingredients
    </h1>
    <p class="paragrafo-lg instrucoes">
Select below the ingredients you need to use in your recipe:
    </p>

    <ul class="categorias">
 <li v-for="categoria in categorias" :key="categoria.nome">
 <CardCategoria 
 :categoria="categoria"
  @adicionar-ingrediente="$emit('adicionarIngrediente', $event)"
  @remover-ingrediente="$emit('removerIngrediente', $event)"
 
 />
 </li>

    </ul>

    <p class="paragrafo dica">
        *Please note, we take into account that you have salt, spices and water at home.
    </p>
    <BotaoPrincipal texto="Search Recipes :)" @click="$emit('buscarReceitas')" />
    </section> 
</template>

<style scoped>
.selecionar-ingredientes {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.titulo-ingredientes {
  color: var(--verde-medio, #3D6D4A);
  display: block;
  margin-bottom: 1.5rem;
}

.instrucoes {
  margin-bottom: 2rem;
}

.categorias {
  margin-bottom: 1rem;
  display: flex;
  justify-content: center;
  gap: 1.5rem;
  flex-wrap: wrap;
}

.dica {
  align-self: flex-start;
  margin-bottom: 3.5rem;
}

@media only screen and (max-width: 767px) {
  .dica {
    margin-bottom: 2.5rem;
  }
}

</style>