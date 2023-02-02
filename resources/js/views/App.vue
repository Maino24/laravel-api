<template>
    <div>
        <WorkInProgress/>

        <!-- Scrivere i dati dei posts -->
        <PostsList :posts="posts" :isLoading="isLoading"/>

    </div>
</template>


<script>

import WorkInProgress from "../components/WorkInProgress.vue";
import PostsList from "../components/posts/PostsList.vue";

export default {
    name: "App",
    components: {
        WorkInProgress,
        PostsList
    },

    data(){
        return {
            posts: [],
            isLoading: false,
        }
    },

    mounted(){
        this.getPosts();
    },

    methods: {
        getPosts(){
            this.isLoading = true
            axios.get('http://127.0.0.1:8000/api/posts')
                .then(res => {
                    //console.log(res.data);
                    this.posts = res.data
                }).catch(err => {
                    console.log(err)
                }).then(()=>{
                    this.isLoading = false
                })
        }
    }
}
</script>

