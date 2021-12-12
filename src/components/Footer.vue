<template>
    <footer >
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
    padding: 5rem 0 0;
    background: $blue_to_left;
    color: #AAAAAA;
    font-size: 14px;
    font-weight: 600;
    position: relative;

    a {
        text-decoration: none;
        color: #FFFFFF;
    }
    h5,
    strong {
        color: #FFFFFF;
    }
    h5 {
        font-size: 16px;
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
        }
    }
    .image_container {
        padding-bottom: 3rem;
    }
    .socials {
        margin-top: 4rem;
        padding: 1.5rem 0 2rem;
        border-top: 1px solid #AAAAAA;
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
                background: #FFFFFF;
                border: 1px solid #000000;

                &:hover {
                    transform: scale(1.1);
                }
                * {
                    color: #000000;
                    font-size: 14px;
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
            color: #FFFFFF;
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