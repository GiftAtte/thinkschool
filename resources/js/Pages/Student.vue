<template>
    <app-layout>
        <template #header>
            <h2 class="h4 font-weight-bold">
            Student
            </h2>
        </template>
              <div class="card card-body">
                  <table class="table">
                  <tr v-for="user in users" :key="user.id">
                         <td>{{user.id}}</td>
                         <td>{{user.name}}</td>
                         <td>{{user.email}}</td>
                  </tr>
                  </table>
              </div>

    </app-layout>
</template>

<script>
    import AppLayout from '@/Layouts/AppLayout'

    export default {
        props:['users'],


        components: {
            AppLayout,

        },
        created(){
            console.log(this.users)
        }
    }
</script>
