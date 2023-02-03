<template>
    <div>


        <router-view></router-view>

    </div>
</template>


<script>

import WorkInProgress from "../components/WorkInProgress.vue";
import PostsList from "../components/posts/PostsList.vue";
import Pagination from "../components/posts/PostsList.vue";

export default {
    name: "App",
    components: {
        WorkInProgress,
        PostsList,
        Pagination
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

