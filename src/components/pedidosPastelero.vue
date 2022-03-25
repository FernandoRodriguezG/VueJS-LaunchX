<template>
    <div class="pedidosPastelero">

        <br>
        <h3>Pedidos para realizar:</h3>
        <ul>
            <li v-for="p in $store.state.pedidos" v-bind:key="p.Nombre">
                {{p.Nombre}} -
                {{p.Telefono}} - 
                {{p.email}} - <br>
                {{p.descripcion}} <br>
                {{p.adornos.vela}} -- 
                {{p.adornos.cantidad}} <br>
                {{p.sabores.primero}} - 
                {{p.sabores.segundo}} - 
                {{p.sabores.tercero}} <br> <br>
            </li>
            
        </ul>
     </div>
</template>

<script>
export default {
    name:'pedidosPastelero',

}
</script>
<style scoped>
ul,li {
    list-style-type: none;
}
</style>