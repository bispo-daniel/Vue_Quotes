<template>
    <footer>
        <p>© Bishop Inc. 2023</p>
    </footer>
</template>

<style>
    footer {
        width: 80%;
        height: 80px;
        
        background-color: #00004066;
        
        border-radius:  5px 5px 0 0;
        border: 1px solid #ffffff66;
        border-bottom: none;
        display: flex;
        align-items: center;
        justify-content: center;

        font-size: 25px;
    }

    @media screen and (max-width: 425px) {
        footer {
            width: 100%;
            border-radius: 0;
        }
    }
</style>