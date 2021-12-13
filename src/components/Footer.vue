<template>
    <footer >
        <!-- Email address section -->
        <div class="email_section container">
            <div class="row align-items-center">
                <div class="col-7">
                    <h3>We Offer Awesome Services</h3>
                    <p>When, While lovelyteems vapour around meand meridians sun strikes the upper surface.</p>
                </div>
                <div class="col-5 input_section">
                    <input class="text_area" type="email" placeholder="Enter Your Email Address">
                    <button class="button button_lg btn_blue">Subscripe</button>
                </div>
            </div>
        </div>
        <!-- Links and contact -->
        <div class="container" id="contact-section">
            <div class="row">
                <div class="col-3">
                    <div class="image_container">
                        <img src="../assets/white-logo-2.png" alt="Phlon Corporate">
                    </div>
                    <p>
                        When, While lovelyteems vapour aroundmeand meridians sun strikes the upper impenetrable
                    </p>
                </div>
                <!-- Links -->
                <div class="col-3">
                    <ul>
                        <h5>Quick Links</h5>
                        <li>
                            <a href="#">
                                Services
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Contact
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Blog
                            </a>
                        </li>
                    </ul>
                </div>
                <!-- Resources -->
                <div class="col-3 d-flex justify-content-center">
                    <h5>Resources</h5>
                    <ul class="pt-5">
                        <li>
                            <a href="#">
                                Art Design
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Computer
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                IT News
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Networking
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Web Security
                            </a>
                        </li>
                    </ul>
                </div>
                <!-- Contact -->
                <div class="col-3">
                    <ul>
                        <h5>Contact Us</h5>
                        <li class="py-4">
                            <strong>Address:</strong> Patricia C.Amedee 4401Waldeck Street Grapevine Nashvile, Tx 76051
                        </li>
                        <li class="pb-0">
                            <strong>Phone:</strong> +99 (0) 101 0000 888
                        </li>
                        <li class="pt-0">
                            <strong>Email:</strong> Info@yourdomain.com
                        </li>
                    </ul>
                </div>
            </div>
        </div>
        <!-- Socials section -->
        <div class="socials">
            <div class="container">
                <div class="row justify-content-between align-items-center">
                    <div class="col-6">
                        &#169; 2020 Phlox. All Rights Reserved.
                    </div>
                    <!-- Socials and chat -->
                    <div class="col-6 d-flex justify-content-end align-items-center">
                        <!-- Social icon -->
                        <div class="col-3 d-flex justify-content-between align-items-center social">
                            <a
                                v-for="element in Socials" :key="element.name"
                                :href="element.link"
                            >
                                <i :class="element.iconClass" class="socila_icon"></i>
                            </a>
                            <div class="arrow_icon">
                                <a href="#top-section">
                                    <i class="fas fa-arrow-up"></i>
                                </a>
                            </div>
                        </div>
                        <!-- Chat -->
                        <div class="col-1 chat">
                            <a href="#">
                                <i class="far fa-comment"></i>

                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
    data() {
        return {
            Socials: [
                {
                    name: 'Instagram',
                    iconClass: 'fab fa-instagram',
                    link: 'https://www.instagram.com',
                },
                {
                    name: 'LinkedIn',
                    iconClass: 'fab fa-linkedin-in',
                    link: 'https://it.linkedin.com',
                },
                {
                    name: 'Facebook',
                    iconClass: 'fab fa-facebook-f',
                    link: 'https://www.facebook.com/',
                },
                {
                    name: 'Twitter',
                    iconClass: 'fab fa-twitter',
                    link: 'https://twitter.com/?lang=it',
                },
            ],
        }
    },
}
</script>

<style scoped lang="scss">
@import '@/styles/Variables';
footer {
    padding: 7rem 0 0;
    background: $blue_to_left;
    color: $gray;
    font-size: 14px;
    font-weight: 600;
    position: relative;

    a {
        text-decoration: none;
        color: $white;
    }
    h5,
    strong {
        color: $white;
    }
    h5 {
        font-size: $big;
        font-weight: 600;
        pointer-events: none;
    }
    ul {
        list-style: none;
        li {
            padding: 0.5rem 0;
        }
        a {
            color: currentColor;

            &:hover {
                color: $white;
            }
        }
    }

    .email_section {
        position: absolute;
        top: 0;
        left: 50%;
        padding: 2.5rem 1rem;
        background: $red_to_right;
        border-radius: 20px;
        transform: translate(-50%, -50%);

        h3 {
            font-weight: 800;
            color: $white;
        }

        p {
            font-size: 13px;
        }

        .input_section {
            position: relative;

            button {
                position: absolute;
                right: 3%;
                top: 12%;
                border-radius: 20px;
            }

            .text_area {
                border-radius: 20px;
                width: 100%;
                padding: 0.375rem 0.75rem;
                line-height: 1.5;
                border: 1px solid #ced4da;
                appearance: none;
                font-size: 1rem;
                font-weight: 400;
                color: currentColor;
                
                &::placeholder {
                    color: $gray;
                }

                &:focus {
                    outline: none;
                }
            }
        }

    }

    .image_container {
        padding-bottom: 3rem;
    }

    .socials {
        margin-top: 4rem;
        padding: 1.5rem 0 2rem;
        border-top: 1px solid $gray;
        .social {
            padding-right: 2rem;
            position: relative;
            .socila_icon:hover {
                transform: scale(1.3);
            }
            .arrow_icon {
                position: absolute;
                left: 100%;
                bottom: 80%;
                width: 35px;
                height: 35px;
                background: $white;
                border: 1px solid $black;

                &:hover {
                    transform: scale(1.1);
                }
                * {
                    color: $black;
                    font-size: $regular;
                }
            }
        }
        .chat {
            display: flex;
            justify-content: center;
            align-items: center;
            width: 55px;
            height: 55px;
            background-color: #527CEB;
            color: $white;
            border-radius: 50%;
            transform: rotateY(180deg);
            font-size: 22px;
            position: absolute;
            right: 2%;
            bottom: 2%;
        }
    }
}
</style>