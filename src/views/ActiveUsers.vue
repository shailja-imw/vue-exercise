<script setup>
import { computed, reactive } from 'vue'

// reactive state
const userList = reactive([{ id: 1, name: 'larry', isActive: true },
{ id: 2, name: 'lisa', isActive: true },
{ id: 3, name: 'john', isActive: true },
{ id: 4, name: 'maddy', isActive: false },
{ id: 5, name: 'mark', isActive: false },
{ id: 6, name: 'jacob', isActive: true },
{ id: 7, name: 'mania', isActive: true },
{ id: 8, name: 'loe', isActive: false },
])

</script>
    
<template>
  <div class="container mt-5">
    <h3>Active users' table</h3>
    <div class="">
      <table class="table m-3">
        <thead class="table-light">
          <tr>
            <th scope="col" class="h4">#</th>
            <th scope="col" class="h4">Name</th>
            <th scope="col" class="h4">username</th>
            <th scope="col" class="h4">Status</th>
          </tr>
        </thead>
        <tbody v-for="(user, index) of userList" :key="index" >
          <tr v-if="user.isActive">
            <th scope="row">{{  user.id  }}</th>
            <td>{{ user.name  }}</td>
            <td>@{{  user.name  }}</td>
            <td>{{ user.isActive ? 'Active' : 'Deactive' }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>
