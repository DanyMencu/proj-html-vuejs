<template>
  <section class="blue_bottom">
    <div class="container">
        <div class="row justify-content-between align-items-center">
            <div class="img_container col-4">
                <img src="../assets/nemoodar.png" alt="Graphic image">
                <img class="over_img" src="../assets/men-data.png" alt="Project image">
            </div>
            <div class="col-5 pt-5">
                <strong>Start Your Project</strong>
                <ul>
                    <li><strong>Grow Your Business</strong></li>
                    <li>With Our Strategy</li>
                </ul>
                <p class="pt-1 pb-4">When, while the lovely valley teems with vapour aroung meand the meridians sun strike the upper surface .of the impenetrable foliage of my trees, and but a few stray gleams steal into the inner sanctuary.</p>
                <button class="button button_md red_right">Try it Now</button>
                <button class="button button_md btn_blue ms-3">Explore More</button>
            </div>
        </div>
    </div>
  </section>
</template>

<script>
export default {
    name: 'ProjectSection',

}
</script>

<style scoped lang="scss">
@import '@/styles/Variables';

.container {
    padding: 6rem 0 13rem;
    color: #FFFFFF;

    .img_container {
        position: relative;

        .over_img {
            position: absolute;
            top: 20%;
            left: 0;
        }
    }

    img {
        width: 100%;
    }

    ul {
        font-size: 36px;
        list-style: none;
        padding-left: 0;
        padding-top: 15px;
    }

    p {
        color: #03A7D3E6;
        font-size: 14px;
    }
}

</style>