<template>
    <div class="blue_bottom" id="top-section">
        <div class="container">
            <div class="row justify-content-between align-items-center">
                <!-- Content section -->
                <div class="col-4">
                    <ul>
                        <li><strong>Business Planning</strong></li>
                        <li>Digital Technology</li>
                        <li><strong>Modedrn Solution!</strong></li>
                    </ul>
                    <p class="pb-4">When, while the lovely valley teems with vapour aroung meand the meridians sun strike the upper surface .</p>
                    <button class="button button_md red_right">Try it Now</button>
                    <button class="button button_md btn_blue ms-3">Explore More</button>
                </div>
                <!-- Image section -->
                <div class="col-5">
                    <img src="../assets/header.png" alt="Hero image">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Hero',
}
</script>

<style scoped lang="scss">
@import '@/styles/Variables';
.container {
    padding: 6rem 0 5rem;
    img {
        width: 100%;
    }
    ul {
        color: $white;
        font-size: 36px;
        list-style: none;
        padding-left: 0;
    }
    p {
        color: #03A7D3E6;
        font-size: $regular;
    }
}
</style>