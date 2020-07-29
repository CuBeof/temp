<template>
    <v-img
        height="200px"
        class="white--text align-center"
        src="@/assets/welcomeback.png"
    >
        <span class="overlay"></span>
        <v-card-title class="layout justify-center">WELCOME BACK</v-card-title>
    </v-img>
</template>

<style scoped>
.overlay {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background-color: #000;
    opacity: .25;
    z-index: -1;
}
</style>