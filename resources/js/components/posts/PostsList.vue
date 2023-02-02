<template>
    <div>
        <!-- Uso il loader -->
        <Loader v-if="isLoading" />
        <ul v-else-if="posts.length">
            <li v-for="elem in posts" :key="elem.id">{{elem.title}}</li>
        </ul>
        <p v-else>Non ci sono psts nel db</p>

    </div>
</template>

<script>

    import Loader from '../Loader.vue'

    export default{
        name: 'PostsList',
        props: ['posts', 'isLoading'],
        components: {
            Loader
        }
    }
</script>

<style scoped lang="scss">

</style>
