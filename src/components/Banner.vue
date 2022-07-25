<template>
    <div id="main-banner">
        <h1>Cadastrado de Produto</h1>
    </div>
</template>

<script>
export default {
    name: "Banner"
}
</script>

<style>

    #main-banner{
        background-image: url('../../public/img/banner.png');
        background-position: 0 ;
        background-size: cover;
        height: 47rem;
        display: flex;
        align-items: center;
        justify-content:flex-start;

    }

    #main-banner h1 {
        color: #fff;
        text-align: center;
        font-size: 60px;
        background-color: #ced133;
        padding: 20px 40px;
    }

</style>