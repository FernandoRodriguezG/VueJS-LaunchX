<template>
    <div class="pedidosCliente"><h3>
        Haz tu pedido:
    </h3>
        Nombre:
        <input type="text" id="name" v-model="$store.state.pedidos.Nombre"><br>
        Telefono:
    <input type="tel" id="phone" name="phone" pattern="[0-9]{3}-[0-9]{3}-[0-9]{4}" v-model="$store.state.pedidos.Telefono"><br>
        Email:
        <input type="email" id="email" v-model="$store.state.pedidos.email"><br>
         Descripcion general del pastel:<input type="text" id="desc" v-model="$store.state.pedidos.descripcion"><br>

         
        Tipo de vela:
        <input type="text" id="velas" v-model="$store.state.pedidos.adornos"><br>
        Cantidad de velas:<input type="text" id="cantvela" v-model="$store.state.pedidos.adornos"><br>



        En caso de no querer los tres sabores, solo llenar los que requieras: <br>
        Primer sabor:<input type="text" id="firstSabor" v-model="$store.state.pedidos.sabores"><br>
        Segundo sabor:<input type="text" id="segSabor" v-model="$store.state.pedidos.sabores"><br>
        Sabor sabor:<input type="text" id="thirdSabor" v-model="$store.state.pedidos.sabores"><br>
        <button @click="$store.commit('addPedido',
        {Nombre:$store.state.adornos.Nombre,
        Telefono:$store.state.pedidos.Telefono,
        email:$store.state.pedidos.email,
        descripcion:$store.state.pedidos.email,
        adornos: $store.state.pedidos.adornos.vela,
        sabores: $store.state.pedidos.sabores.segundo
        })">
        Hacer pedido</button>
        
        
     </div>
</template>

<script>
export default {
    name:'pedidosCliente',

}
</script>
<style scoped>
ul,li {
    list-style-type: none;
}
</style>