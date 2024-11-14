<script lang="ts">
    import { goto } from '$app/navigation';

function submitForm(event:Event) {
   event.preventDefault();
   navigateToResetPage();
}

function navigateToResetPage() {
   goto("/password/reset")
}
</script>

<section class="flex justify-center items-center  h-screen">
    <div class="w-screen md:w-2/3 lg:w-[522px] m-4  flex flex-col justify-evenly">

        <div class="text-center h-1/3 flex flex-col justify-center">
            <h1>Note App</h1>
            <p class="mt-2 text-2xl font-bold">Forgotten your password?</p>
        <p class="mt-2 text-gray-500">Enter your email below, and we’ll send you a link to reset it.</p>
    </div>
 
    <!-- Formulaire de connexion -->
    <form class="flex flex-col" on:submit={submitForm}>
        <label for="mailInput" class="mb-1 font-semibold">Email Address</label>
        <input id="mailInput" type="email" class="border-2 rounded h-10 ps-4" placeholder="email@example.com"/>
        <button class="rounded bg-blue-700 h-12 mt-4 text-white font-bold" type="submit">Send Reset Link</button>
    </form>
</div>

</section>