<template>
    <section class = "footer-area">
        <div>
            <div class="copyright-info">
                &copy; 2018 Retrospective Action Notes
            </div>
            <!-- <div class = "social-media-icons"> -->
                <!-- Add icon library -->
                <!-- <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css"> -->

                <!-- Add font awesome icons -->
                <!-- <a href="#" class="fa fa-facebook-official"></a>
                <a href="#" class="fa fa-youtube"></a>
                <a href="#" class="fa fa-snapchat"></a>  -->
           <!-- </div>  -->
        </div>
    </section>
</template>
    

<script>

</script>

<style lang="scss" scoped>
    @import '../scss/_variables.scss';

    .footer-area {
        background: $lightGrey;
        // min-width: calc(100% - 1px);
        width: 100%;
        height: 20%;
        position: absolute;
        bottom: 0;

        .copyright-info {
            font-family: "OpenSans";
            font-size: 12px;
            display: flex;
            justify-content: space-around;
            align-items: flex-end;
        }

        .social-media-icons {
            .fa {
                padding: 20px;
                font-size: 25px;
                width: 8px;
                height: 8px;
                text-decoration: none;
                margin: 5px ;
                border-radius: 50%;
            }
            .fa:hover {
                opacity: 0.7;
            }
            
            .fa-facebook:before {
                font-size:48px;


            }

            .fa-youtube {

            }

            .fa-snapchat {

            }

        }

    }

    
</style>
