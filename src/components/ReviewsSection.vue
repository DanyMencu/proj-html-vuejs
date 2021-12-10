<template>
  <section>
      <div class="container">
          <!-- Header section -->
          <div class="row justify-content-center align-items-center">
                <div class="col-6 text-center header_section">
                    <span>Testimonial</span>
                    <p class="text"><strong>What</strong> People Say</p>
                    <p>When, while the lovely valley teems with vapour aroung meand the upper surface .</p>
                </div>
          </div>

          <!-- Review section -->
          <div class="row justify-content-center align-items-center">
              <div class="col-4 ">
                  <div class="review">
                    <div class="img_profile">
                        <img src="../assets/szabo-viktor-1266895-unsplash-1024x1024.png" alt="Lorem">
                    </div>
                    <div class="rating">
                        <i class="fas fa-star"></i>
                        <i class="far fa-star"></i>
                    </div>
                    <p class="text">
                        When, while the lovely valley teems with vapor around me, and the maridian sun strikes the upper impenetrable foliage of my trees, and but a thousand.
                    </p>
                    <span class="author">
                        Michkel Anegl
                    </span>
                    <span class="role">
                        Marketing Management
                    </span>
                  </div>
              </div>
          </div>
      </div>
  </section>
</template>

<script>
export default {
    name: 'ReviewsSection',
    data() {
        return {
            Reviews: [
                {
                    image: require('@/assets/szabo-viktor-1266895-unsplash-1024x1024.png'),
                    rating: 3,
                    text: 'When, while the lovely valley teems with vapor around me, and the maridian sun strikes the upper impenetrable foliage of my trees, and but a thousand.',
                    author: 'Michkel Anegl',
                    role: 'Marketing Management',
                },
                {
                    image: require('@/assets/philipe-cavalcante-539505-unsplash-1024x1024.png'),
                    rating: 3,
                    text: 'When, while the lovely valley teems with vapor around me, and the maridian sun strikes the upper impenetrable foliage of my trees, and but a thousand.',
                    author: 'Michkel Anegl',
                    role: 'Marketing Management',
                },
                {
                    image: require('@/assets/fabio-spinelli-695744-unsplash-1024x1024.png'),
                    rating: 3,
                    text: 'When, while the lovely valley teems with vapor around me, and the maridian sun strikes the upper impenetrable foliage of my trees, and but a thousand.',
                    author: 'Michkel Anegl',
                    role: 'Marketing Management',
                },
            ]
        }
    },

}
</script>

<style scoped lang="scss">
@import '@/styles/Variables';

section {
    padding: 1rem 0 5rem;

    .header_section {
        padding-bottom: 2rem;

        span {
            color: #B6246E;
            font-size: 12px;
        }

        .text {
                font-size: 34px;
        }

        p {
            font-size: 14px;
        }
    }
}

.review {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    .img_profile {
        width: 80px;
        height: 80px;
        border: 3px solid $primary_red;
        border-radius: 50%;
        overflow: hidden;

        img {
            width: 100%;
            object-fit: cover;
        }
    }

    .rating {
        color: $primary_red;
        padding: 2rem 0;
    }

    .text {
        text-align: center;
    }

    .author {
        font-weight: 600;
        padding: 1rem 0 0.5rem;
    }
}
</style>