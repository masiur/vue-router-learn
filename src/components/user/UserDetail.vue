<template>
    <div>
        <h3>Some User Details</h3>
        <p>User loaded id: {{ $route.params.id }}</p>
        <router-link 
            tag="button"
            :to="{ name: 'userEdit', params: { id:$route.params.id }, query: { locale: 'bn', q: 100}}"
            class="btn btn-success"
            >Edit User</router-link>
    </div>
</template>