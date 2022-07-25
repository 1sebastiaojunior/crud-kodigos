<template>
  <div>
    <div>
      <form id="produto-form" @submit="createProduto">
        <div class="input-container">
          <label for="nome">Nome do Produto: </label>
          <input
            type="text"
            id="nome"
            name="nome"
            v-model="nome"
            placeholder="Digite o nome do Produto..."
          />
        </div>
        <div class="input-container">
          <label for="descricao">Descrição: </label>
          <textarea
            type="text"
            id="descricao"
            name="descricao"
            size="50"
            v-model="descricao"
            placeholder="Descrição do produto"
          ></textarea>
        </div>
        <div class="input-container">
          <label for="unidademedida">Unidade de Medida: </label>
          <input
            type="text"
            id="unidademedida"
            name="unidademedida"
            v-model="unidademedida"
            placeholder="Unidade de medida do produto"
          />
        </div>
        <div class="input-container">
          <input type="submit" class="submit-btn" value="Cadastrar Produto" />
        </div>
      </form>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: "ProdutoForm",
  data() {
    return {
      nomes: null,
      descricoes: null,
      unidadesmedida: null,
      nome: null,
      descricao: null,
      unidademedida: null,
    };
  },
  methods: {
    async createProduto(e) {
      e.preventDefault();

      const data = {
        nome: this.nome,
        descricao: this.descricao,
        unidademedida: this.unidademedida,
      };

      axios
        .post("http://localhost:3000/produtos", {
          nome: this.nome,
          descricao: this.descricao,
          unidademedida: this.unidademedida,
        })
        .then(function (response) {
          console.log(response);
        })
        .catch(function (error) {
          console.log(error);
        });

    },
  },
};
</script>

<style scoped>
#produto-form {
  max-width: 400px;
  margin: 0 auto;
}

.input-container {
  display: flex;
  flex-direction: column;
  margin-bottom: 20px;
}

label {
  font-weight: bold;
  margin-bottom: 15px;
  color: #222;
  padding: 5px 10px;
  border-left: 4px solid #0e206b;
}

input {
  padding: 5px 10px;
  height: 50px;
}

.submit-btn {
  background-color: #0e206b;
  color: #ced133;
  font-weight: bold;
  border: 2px solid #222;
  border-radius: 25px;
  padding: 10px;
  font-size: 16px;
  margin: 0 auto;
  cursor: pointer;
  transition: 0.5s;
}

.submit-btn:hover {
  background-color: transparent;
  color: #0e206b;
}
</style>