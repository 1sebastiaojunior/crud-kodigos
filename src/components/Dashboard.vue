<template>
    <div id="produto-table">
        <div>
            <div id="produto-table-heading">
                <div class="order-id">Id</div>
                <div>Nome</div>
                <div>Descrição</div>
                <div>Unidade de medida</div>
                <div>Ações</div>
            </div>
        </div>
        <div id="produto-table-rows">
            <div class="produto-table-row">
                <div class="order-number">1</div>
                <div>Pão</div>
                <div>francês</div>
                <div>kg</div>
                <button class="update-btn">Editar</button>
                <button class="delete-btn">Deletar</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Dashboard"
}
</script>

<style scoped>
   #produto-table {
    max-width: 1200px;
    margin: 0 auto;
   } 

   #produto-table-heading,
   #produto-table-rows,
   .produto-table-row {
    display: flex;
    flex-wrap: wrap;
   }

   #produto-table-heading {
    font-weight: bold;
    padding: 12px;
    border-bottom: 3px solid #333;
   }

   #produto-table-heading div,
   .produto-table-row div {
    width: 20%;
   }

   .produto-table-row {
    width: 100%;
    padding: 12px;
    border-bottom: 1px solid #ccc;
   }

   #produto-table-heading .order-id,
   .produto-table-row .order-number {
    width: 5%;
   }

   .update-btn {
    background-color: #0e206b;
    color: #ccc;
    font-size: bold;
    border: 1px solid #333;
    border-radius: 15px;
    padding: 6px;
    font-size: 16px;
    margin: 0 auto;
    cursor: pointer;
    transition: .5s;
   }

   .update-btn:hover {
    background-color: transparent;
    color: #0e206b;
   }

   .delete-btn {
    background-color: #971717;
    color: #ccc;
    font-size: bold;
    border: 1px solid #333;
    border-radius: 15px;
    padding: 6px;
    font-size: 16px;
    margin: 0 auto;
    cursor: pointer;
    transition: .5s;
   }

   .delete-btn:hover {
    background-color: transparent;
    color: #971717;
   }
</style>