<template>
    <div class="d-flex text-center flex-column flex-md-row flex-grow-1" :style="{
        backgroundSize: 'cover',
        backgroundImageAlt: `${backgroundImage}`,
        backgroundImage: `url(${image})`,
        backgroundPosition: 'center center',
        backgroundRepeat: 'no-repeat',
        backgroundAttachment: 'fixed'
    }">

    <div>

    </div>

    </div>
</template>
<script>
import {mapState} from 'vuex'
export default {
    data() {
        return {
            backgroundImage: "",
        }
    },
    computed: {
        ...mapState(['isMobile']),

        image() {
            return this.isMobile ? "/fondo-login.jpg" : "https://previews.123rf.com/images/armpannawat/armpannawat1508/armpannawat150800036/43724743-mesa-de-madera-vac%C3%ADa-y-moderno-fondo-de-biblioteca-pantalla-de-montaje-de-productos.jpg";
        }
    }
}
</script>
<style lang="scss" scoped>

</style>>

</style>