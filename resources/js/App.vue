
    <script>
    import {store} from './store/store.js';
    import axios from 'axios';

    export default {
        name: 'App',

        methods:{
            getApi(){
                axios.get(store.apiUrl + 'posts')
                .then(results => {
                    this.posts = results.data;
                    console.log(this.posts)
                })
            }
        },

        mounted(){
            this.getApi();
        }
    }
    </script>

    <template>
        <h1>Home</h1>
    </template>

    <style>

    </style>
