<template>
    <div>
<h1>{{title}}</h1>
<slot></slot>
    </div>
</template>

<script>
    export default {
        // eslint-disable-next-line vue/multi-word-component-names
        name: "Card",
        props:["title"]
        
    }
</script>

<style scoped>

</style>