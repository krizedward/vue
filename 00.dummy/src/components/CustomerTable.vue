//CustomerTable.vue
<template>
    <table class="table">
        <thead class="thead-light">
            <tr>
                <th scope="col">Nama</th>
                <th scope="col">Email</th>
                <th scope="col">Alamat</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Bambang</td>
                <td>bambang@mail.com</td>
                <td>Jl.Kenanga</td>
            </tr>
            <tr>
                <td>Dika</td>
                <td>dika@mail.com</td>
                <td>Jl.Mangga</td>
            </tr>
            <tr>
                <td>Agus</td>
                <td>agus@mail.com</td>
                <td>Jl.Mataram</td>
            </tr>
        </tbody>
        <!-- Selanjutnya kita akan merender data array dari props customers dan membuat loop. Silahkan buka komponen CustomerTable.vue dan buat seperti dibawah ini. -->
        <!-- <tbody>
            <tr v-for="customer in customers" :key="customer.id"> 
                <td>{{ customer.name }}</td>
                <td>{{ customer.email }}</td>
                <td>{{ customer.address }}</td>
            </tr>  
        </tbody> -->
    </table>
</template>

<script>
export default {
    name: 'customer-table',
    // Props adalah cara kita meneruskan data dari komponen induk ke komponen anak.
    props: {
        customers: Array,
    },
}
</script>

<style scoped>

</style>