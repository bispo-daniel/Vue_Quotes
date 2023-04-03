<template>
    <header class="MyHeader">
        <img src="@/assets/logo.svg" alt="" width="60" height="60">
    </header>
</template>

<style>
    .MyHeader {
        width: 80%;
        height: 80px;
        
        background-color: #043927;

        border-radius: 0 0 5px 5px;

        display: flex;
        align-items: center;

        margin-bottom: 20px;
    }
    .MyHeader > img {
        padding-left: 20px;
    }

    @media screen and (max-width: 425px) {
        .MyHeader {
            width: 100%;
            border-radius: 0;
        }
    }
</style>