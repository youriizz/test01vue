<template>
    <div class="RedCircle" @click="navigate"></div>
</template>

<script>
export default {
    name: 'RedCircle',
    methods: {
        navigate() {
            window.location.href = 'https://google.com';
        }
    }
}
</script>

 <style scoped>

.RedCircle {
    width: 50px;
    height: 50px;
    background-color: red;
    border-radius: 50%;
    cursor: pointer;
    transition: background-color 0.3s;
}

.RedCircle:hover {
    background-color: blue;
}

</style>