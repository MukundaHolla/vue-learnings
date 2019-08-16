<template>
    <div class="blogs">
        <h2>{{ blogTitle }}</h2>
        <button @click="changeTitle">click me!</button>
    </div>
</template>

<script>
export default {
    name: 'Blogs',
    data() {
        return {
            blogTitle: 'Blogs'
        }
    },
    methods: {
        changeTitle() {
            this.blogTitle = 'Amazing'
        }
    },
    beforeCreate() {
        alert('beforeCreate Hook')
    },
    created() {
        alert('Created')
    },
    beforeUpdate() {
        alert('before update')
    }
}
</script>