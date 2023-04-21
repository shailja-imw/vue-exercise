<template>
    <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
            <RouterLink class="nav-link active" aria-current="page" to="/">Home</RouterLink>
        </li>
        <li class="nav-item">
            <RouterLink class="nav-link" to='/active-users'>Active Users</RouterLink>
        </li>
        <li class="nav-item">
            <RouterLink class="nav-link" to='/login' tabindex="-1" aria-disabled="true">Login</RouterLink>
        </li>
    </ul>
</template>
