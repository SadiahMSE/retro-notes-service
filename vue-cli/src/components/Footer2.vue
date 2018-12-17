<template>
    <section class = "footer-area">
        <div>
            <div class="copyright-info">
                &copy; 2018 Retrospective Action Notes
            </div>
        </div>
    </section>
</template>

<script>
</script>

<style lang="scss" scoped>
 @import '../scss/_variables.scss';

    .footer-area {
        background: $lightGrey;
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
    }

</style>