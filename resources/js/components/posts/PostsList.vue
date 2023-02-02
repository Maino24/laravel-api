<template>
    <div>
            <ul>
                <li v-for="elem in posts" :key="elem.id">{{elem.title}}</li>
            </ul>
        </div>
</template>

<script>
    export default{
        name: 'PostsList',
        props: ['posts']
    }
</script>

