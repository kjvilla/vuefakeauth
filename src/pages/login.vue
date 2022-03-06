<template>
    <div class ="flex flex-col space-y-12 items-center justify-center min-h-screen-nonav">
        <h2 class="text-6xl tracking-tighter font-extralight">Login</h2> 
        <div class="flex items-center justify-center bg-gray-200 overflow-hidden rounded-lg shadow-2xl">
            <img class="h-64" src="../assets/bglogin.png" alt="Hello BG" >
            <form class="flex flex-col space-y-4 p-4">
                <input type="text" class="p-2 border-2 rounded-lg" placeholder="Username">
                <input type="password" class="p-2 border-2 rounded-lg" placeholder="Password">
                <button type="submit" class="py-2 rounded-lg bg-purple-500 font-bold" >Login</button>
                </form>  
        </div>
    </div>
</template>
