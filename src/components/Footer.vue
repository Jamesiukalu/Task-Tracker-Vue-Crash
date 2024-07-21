<template>
    <footer>
        <p>Copyright &copy; 2024</p>
        <router-link to="/about">About</router-link>
    </footer>
</template>

<script>
export default {
    name: 'FooterItem'
}
</script>

<style>
a {
    color: #333
}
footer {
    margin-top: 30px;
    text-align: center;
}
</style>