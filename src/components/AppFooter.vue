<template>
    <footer id="footer">
        <div class="footer-top">
            <div class="container">
                <div class="row">

                    <div class="col-lg-3 col-md-6 footer-contact">
                        <img src="../assets/images/white-logo-2.png" alt="white-logo" width="30" height="24"
                            class="d-inline-block align-text-top" id="logo-navbar">
                        <p>When, while lovely valley teems vapour aroundmeand meridian sun strikes the upper impenetrable
                        </p>
                    </div>

                    <div class="col-lg-3 col-md-6 footer-links">
                        <h4>Quick Links</h4>
                        <ul>
                            <li><i class="bx bx-chevron-right"></i> <a href="#">Services</a></li>
                            <li><i class="bx bx-chevron-right"></i> <a href="#">Contact</a></li>
                            <li><i class="bx bx-chevron-right"></i> <a href="#">Blog</a></li>
                        </ul>
                    </div>

                    <div class="col-lg-3 col-md-6 footer-links">
                        <h4>Contact Us</h4>
                        <ul>
                            <li><i class="bx bx-chevron-right"></i> <a href="#"><span>Address : </span> Patricia C. Amedee
                                    4401 Waldeck Street Grapevine Nashville, Tx 76051</a></li>
                            <li><i class="bx bx-chevron-right"></i> <a href="#"><span>Phone: </span> +99 (0) 101 0000
                                    888</a></li>
                            <li><i class="bx bx-chevron-right"></i> <a href="#"><span>Email: Info@yourdomain.com</span></a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>

        <div class="container footer-bottom clearfix">

            <div class="copyright">
                <span><i class="fa-regular fa-copyright"></i> Phlox. All Rights Reserved.</span>
            </div>

            <div class="col-lg-3 col-md-6 footer-links">
                <div class="social-links mt-3">
                    <a href="#" class="instagram"><i class="fa-brands fa-instagram"></i></a>
                    <a href="#" class="linkedin"><i class="fa-brands fa-linkedin"></i></a>
                    <a href="#" class="facebook"><i class="fa-brands fa-facebook"></i></a>
                    <a href="#" class="twitter"><i class="fa-brands fa-twitter"></i></a>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
import { store } from '../store.js'

export default {
    name: 'AppFooter',

    components: {

    },

    data() {

        return {
            store,
        };
    },

    methods: {

    }
}
</script>


<style lang="scss" scoped>
#footer {
    padding-top: 100px;
    font-size: 14px;
    background-color: #020331;

    .footer-top {
        padding: 60px 0 30px 0;

        .footer-contact h4,
        .footer-links h4 {
            font-weight: bold;
            color: #fff;
        }

        .footer-links ul {
            list-style: none;
            padding: 0;
            margin: 0;

            li {
                padding: 10px 0;
                display: flex;
                align-items: center;

                &:first-child {
                    padding-top: 0;
                }

                a {
                    color: #777777;
                    transition: 0.3s;
                    display: inline-block;
                    line-height: 1;
                }
            }
        }
    }

    .footer-bottom {
        padding-top: 30px;
        padding-bottom: 30px;
        color: #fff;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .copyright {
        float: left;
    }

    .credits {
        float: right;
        font-size: 13px;
    }
}
</style>    