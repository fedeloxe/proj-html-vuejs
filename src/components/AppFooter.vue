<script>
export default {

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
                <input type="submit" value="Submit" class="submit">


            </div>
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
            padding: 14px 20px;
            margin: 8px 0;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        .text {
            width: 100%;
            padding: 12px 20px;
            margin: 8px 0;
            display: inline-block;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }
    }
}
</style>