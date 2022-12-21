<template>
    <p>{{ pesan }}</p>
</template>

<script>
export default {
    props:{
        pesan:{
            type: String,
            default: "",
        }
    }
}</script>