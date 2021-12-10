<template>

<div class="col-3 post "
    :class="ActiveIndex === index ? 'active' : false"
>
    <div class="content">
        <div class="date_author">
            {{ date }} 
            <i class="fas fa-circle dot"></i> 
            by {{ author }}
        </div>
        <h3 class="title">
            {{ title }}
        </h3>
        <p class="text">
            {{ text }}
        </p>
    </div>
    <div>
        <button 
            class="button button_md btn_white"
            @click="SetActiveIndex(index)"
        >
            Read More
        </button>
    </div>
        <div class="background_active">
        <img :src="image" :alt="title">
    </div>
</div>

</template>

<script>
export default {
    name: 'CardPost',
    props: {
        image: String,
        title: String,
        text: String,
        author: String,
        date: String,
        index: Number,
    },
    created() {
        this.SetActiveIndex();
    },
    data() {
        return {
            ActiveIndex: 0,
        }
    },
    methods: {
        SetActiveIndex(index) {
            this.ActiveIndex = index;
        }
    },
}
</script>

<style scoped lang="scss">
@import '@/styles/Variables';

.active {
    flex-grow: 1;

    .content {
        max-width: 70%;
    }
}

.post {
    position: relative;
    display: flex;
    align-items: flex-end;
    flex-wrap: wrap;
    padding: 2rem 1.5rem;
    border-radius: 20px;
    margin: 0 10px;
    background: $blue_to_bottom;
    color: #FFFFFF;

    &.active > .background_active{
        opacity: 1;
    }

    &.active > .content h3 {
        padding: 0;
    }

    .content {
        z-index: 2;
        font-size: 16px;
        .date_author {
            padding-bottom: 1rem;
            font-size: 14px;

            .dot {
                font-size: 5px;
                transform: translateY(-50%)
            }
        }

        h3 {
            padding: 2rem 0;
        }
    }

    button {
        z-index: 2;
        position: relative;
        margin-top: 2rem;
    }

    .background_active {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        opacity: 0;

        &::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: #00000065;
            border-radius: 20px;
        }

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 20px;
        }
    }
}

</style>