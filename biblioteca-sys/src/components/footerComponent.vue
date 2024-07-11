<template>
    <div class="text-light custom-bg-dark footer">
        <div> Design in {{  new Date().getFullYear() }}</div>
    </div>
</template>

<style scoped>
.custom-bg-dark{
    background-color: #a3130d;
}

.footer{
    bottom: 0;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 56px;
}
</style>