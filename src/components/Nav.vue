<script setup>
import useAuth from "../useAuth";
const {isAuthenticated, logout} = useAuth();
</script>


<template>
    <div class="bg-zinc-900 text-purple-200">
        <div class="container mx-auto flex items-center justify-between">
            <h1 class="tracking-tighter text-3xl font-thin"><span class="text-lg font-extralight">Vue</span>Fake<span class="font-normal">Auth</span></h1>
            <nav>
                <ul class="flex space-x-4">
                    <router-link to="/">
                    <li class="py-8 px-4 hover:cursor-pointer hover:bg-purple-500 hover:text-purple-800">Home 
                    </li>
                    </router-link>
                    <router-link to="/About">
                    <li class="py-8 px-4 hover:cursor-pointer hover:bg-purple-500 hover:text-purple-800">About
                    </li>
                    </router-link>
                    <router-link v-if="!isAuthenticated" :to="{ path: '/login', name: 'Login' }">
                    <li class="py-8 px-4 hover:cursor-pointer hover:bg-purple-500 hover:text-purple-800">Login
                    </li>
                    </router-link>
                    <router-link v-else :to="{name: 'Secret'}">
                    <li class="py-8 px-4 hover:cursor-pointer hover:bg-purple-500 hover:text-purple-800">Secret
                    </li>
                    </router-link>
                    <button v-else@click="logout">
                        <li class="py-8 px-4 hover:cursor-pointer hover:bg-purple-500 hover:text-purple-800">Logout
                    </li>
                    </button>
                </ul>
            </nav>
        </div>
    </div>
</template>