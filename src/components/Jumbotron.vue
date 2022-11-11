<script>
export default {
    name: 'Jumbotron',
}
</script>

<template>
    <div class="jumbotron ms_jumbo">
        <div class="ms_layover"></div>
        <div class="container ms_container">
            <p class="lead">
                <span class="rounded-0 text-uppercase fw-bold">Current
                    Series</span>
            </p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;



.jumbotron.ms_jumbo {
    height: 500px;
    background-image: url(../assets/img/jumbotron.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center top;
    position: relative;

    .ms_layover {
        position: absolute;
        top: 0;
        left: 0;
        bottom: 0;
        right: 0;
        background-color: rgba($dark, 0.4);
        z-index: 0;
    }

    .container.ms_container {
        height: 100%;
        position: relative;

        p {
            margin: 0;

            span {
                color: $light;
                position: absolute;
                bottom: 0;
                left: 0;
                translate: 0 50%;
                padding: 0.5rem;
                background-color: $primary-color;

                &:hover {
                    color: light;
                }
            }
        }



    }
}
</style>