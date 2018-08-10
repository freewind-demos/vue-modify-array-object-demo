<template>
    <div class="hello">
        <ul>
            <li v-for="user in users" v-on:click="clickUser(user)" class="user">
                {{user}}
            </li>
        </ul>
    </div>
</template>

<script lang="ts">
    import {Component, Prop, Vue} from 'vue-property-decorator';

    type User = {
        name: string,
        clicked?: boolean
    }

    @Component
    export default class HelloWorld extends Vue {
        @Prop() private users: Array<User> = [{name: "Mike"}, {name: "Ann"}];

        clickUser(user: User) {
            // user.clicked = true
            Vue.set(user, 'clicked', true)
        }
    }
</script>

<style scoped>
    .user:hover {
        cursor: pointer;
        background-color: antiquewhite;
    }
</style>
