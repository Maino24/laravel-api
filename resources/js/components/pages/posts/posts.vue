<template>
    <div>
        <WorkInProgress/>

        <!-- Scrivere i dati dei posts -->
        <PostsList/>
    </div>
</template>

<script>

import PostsList from "../../posts/PostsList.vue";

export default {
    name: "Posts",
    components: {
        PostsList,
    },

    data(){
        return {

        }
    },

    mounted(){

    },

    methods: {

    }
}
</script>
