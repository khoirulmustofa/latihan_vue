<template>
    <div>Ini dari Child Component</div>
    <div>{{ pesan }}</div>
</template>

<script>

export default {
    props:{
        pesan:{
            type: String,
            default: "",
        }
    }
}
</script>