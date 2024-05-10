<template>
    <div class="RedCircle" @click="navigate">{{ CircleText }}</div>
</template>

<script>
export default {
    props: ['CircleText'],
    name: 'RedCircle',
    methods: {
        navigate() {
            window.location.href = 'https://google.com';
        }
    }
}
</script>

/* Dans RedCircle.vue */
<style scoped>
.RedCircle {
    width: 150px;
    height: 150px;
    background-color: red;
    border-radius: 50%;
    cursor: pointer;
    transition: background-color 0.7s ease, border-radius 0.7s ease; /* Transition pour le fond et le bord */
    display: flex;
    align-items: center; /* Centre verticalement le texte */
    justify-content: center; /* Centre horizontalement le texte */
    color: rgb(255, 255, 255); /* Couleur du texte */
    font-family: 'Helvetica Neue'; /* Police du texte */
    font-weight: 600;
    font-size: 20px; /* Taille du texte */
}

.RedCircle:hover {
    background-color: blue;
    border-radius: 10%;
}
</style>
