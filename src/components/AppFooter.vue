<script>
import AppLiFooter from './AppLiFooter.vue';

export default {
    components: {
        AppLiFooter,
    },
    data() {
        return {
            footerLink: [
                {
                    title: 'My Account',
                    content: [
                        `<a href=""> My Account </a>`,
                        `<a href=""> Checkout </a>`,
                        `<a href=""> Cart </a>`,
                        `<a href=""> Packages </a>`,
                        `<a href=""> Add Car </a>`,

                    ]
                },
                {
                    title: 'Quick Links',
                    content: [
                        `<a href=""> Home</a>`,
                        `<a href=""> About Us</a>`,
                        `<a href=""> Blog</a>`,
                        `<a href=""> Contact</a>`,
                        `<a href=""> Refound & Returns</a>`,
                    ]
                }
            ]
        }
    }

}
</script>
<template>
    <footer>
        <div class="main-foot">
            <div class="socials">
                <img src="../assets/logo-footer-autocar11.png" alt="logofooter">
                <div class="social">
                    <i class="fa-solid fa-location-dot"></i>
                    <span>New Jersey, USA</span>
                </div>
                <div class="social">
                    <i class="fa-solid fa-phone-volume"></i>
                    <span>1 (234) 567 89 10</span>
                </div>
                <div class="social">
                    <i class="fa-regular fa-envelope"></i>
                    <span>example@example.com</span>
                </div>
                <div class="social-icons">
                    <i class="fa-brands fa-facebook-f"></i>
                    <i class="fa-brands fa-instagram"></i>
                    <i class="fa-brands fa-twitter"></i>
                </div>
            </div>
            <div class="newsletter">
                <h2> Join Our Newsletter </h2>
                <p> Subscribe to be informed about our services and products.</p>
                <input type="" placeholder="Your Email Address" class="text">
                <input type="submit" value="Subscribe &rarr;" class="submit">
            </div>
            <div>
                <AppLiFooter :footerLink="footerLink" />
            </div>
        </div>
        <div class="copyright">
            <p>&#169;2022 Autocar - All Rights Reserved. </p>

        </div>

    </footer>

</template>
<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

footer {
    width: 100%;
    background-color: $black;

    .main-foot {
        width: 75%;
        margin: 20px auto;
        padding: 50px 0;
        display: flex;
        justify-content: space-between;

        .socials {
            color: white;

            .social {
                display: flex;
                align-items: flex-start;
            }


            i {
                font-size: 30px;
                padding: 0 15px 20px 0;
            }

            img {
                height: 70px;
                margin-bottom: 20px;
            }

            .social-icons {
                i {
                    padding: 0 20px;
                }
            }
        }

        .newsletter {
            color: $white;
        }

        .submit {
            width: 100%;
            background-color: $white;
            color: $grey;
            padding: 20px 20px;
            margin: 2px 0;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        .text {
            width: 100%;
            padding: 20px 20px;
            margin: 2px 0;
            display: inline-block;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }
    }

    .copyright {
        width: 15%;
        color: $white;
        margin: 0 auto;
        padding: 10px 0;

    }
}
</style>