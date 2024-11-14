<script lang="ts">
    import { goto } from '$app/navigation';

 function submitForm(event:Event) {
    event.preventDefault();
    navigateToHomePage();
 }

 function navigateToHomePage() {
    goto("/home")
 }
</script>

<section class="flex justify-center items-center  h-screen">
    <div class="h-[603px] w-screen md:w-2/3 lg:w-[522px] m-4  flex flex-col justify-evenly">

        <div class="text-center h-1/3 flex flex-col justify-center">
            <h1>Note App</h1>
            <p class="mt-2 text-2xl font-bold">Welcome to Note</p>
        <p class="mt-2 text-gray-500">Please log in to continue</p>
    </div>
    
    <form class="flex flex-col h-1/3" on:submit={submitForm}>
        <label for="mailInput" class="mb-1 font-semibold">Email Address</label>
        <input id="mailInput" type="email" class="border-2 rounded h-10 ps-4" placeholder="email@example.com"/>
        <div class="flex justify-between mt-4">
            <label for="passwordInput" class="mb-1 font-semibold">Password</label>
            <a href="/forgot" class="text-gray-500 underline">Forgot</a>
        </div>
        <input id="passwordInput" type="password" class="border-2 rounded h-10 ps-4"/>
        <button class="rounded bg-blue-700 h-12 mt-4 text-white font-bold">Login</button>
    </form>
    
    <div class="flex flex-col justify-center text-center h-1/3">
        <p class="text-gray-500">Or log in with:</p>
        <button class="border-2 rounded-lg h-12 font-bold my-4">Google</button>
        <p class="text-gray-500">No account yet? <a href="/sign-up" class="text-black">Sign Up</a></p>
    </div>
</div>

</section>