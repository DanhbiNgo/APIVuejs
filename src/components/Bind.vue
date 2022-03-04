<template>
    <div>
        <a v-bind:href="link" >{{noidung}}</a>
    </div>
</template>
<script>

// v-bind: xử lí link
export default {
    data(){
        return {
                noidung: 'helo',
                link: 'https://www.google.com'
            
        }
    }
}
</script>
<style scoped>

</style>