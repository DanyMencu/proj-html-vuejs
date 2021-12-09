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
                    <a href="#">Home</a>
                    <a href="#">About</a>
                    <a href="#">Services</a>
                    <a href="#">Blog</a>
                    <a href="#">Contact</a>
                    <a href="#">Portfolio</a>
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
.navbar {
    background-color: #00000028;
}

a {
    text-decoration: none;
    color: #FFFFFF;


}
</style>