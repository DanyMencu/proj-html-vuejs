<template>
    <nav class="navbar fixed-top">
        <div class="container pt-2">
            <div class="row w-100">
                <div class="col-6">
                    <a href="#">
                        <img src="../assets/white-logo-2.png" alt="Phlox Corporate">
                    </a>
                </div>
                <div class="col-6 d-flex justify-content-between align-items-center">
                    <a href="#top-section">Home</a>
                    <a href="#project-section">About</a>
                    <a href="#service-section">Services</a>
                    <a href="#blog-section">Blog</a>
                    <a href="#contact-section">Contact</a>
                    <a href="#portfolio-section">Portfolio</a>
                    <a href="#">
                        <button class="button button_sm btn_blue">Sing In</button>
                    </a>
                </div>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
    name: 'Header',
}
</script>

<style scoped lang="scss">
@import '@/styles/Variables';
.navbar {
    background: #0a164ff5;
}
a {
    text-decoration: none;
    color: #FFFFFF;
    &:hover {
        color: $secondary_red;
    }
}
</style>