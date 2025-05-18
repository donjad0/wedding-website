<script lang="ts">
    let password = '';
    let error = '';

    function handleLogin() {
        // You can change this password to whatever you want
        if (password === import.meta.env.VITE_WEBSITE_PASSWORD) {
            window.location.href = '/dashboard';
        } else {
            error = 'Incorrect password. Please try again.';
            password = '';
        }
    }
</script>

<div class="min-h-screen flex flex-col items-center justify-center bg-wedding-background">
    <div class="text-center mb-12 animate-fade-in">
        <h1 class="text-4xl mb-4">Joe & Jade</h1>
        <p class="text-xl">May 29th 2026</p>
    </div>

    <div class="bg-white/80 backdrop-blur-sm p-8 rounded-xl shadow-lg max-w-md w-full mx-4 animate-fade-in-delay-2">
        <h2 class="text-2xl mb-6 text-center">Welcome to Our Wedding Website</h2>
        
        <form on:submit|preventDefault={handleLogin} class="space-y-6">
            <div>
                <label for="password" class="block text-sm font-medium text-gray-700 mb-2">
                    Please enter the password shared in your invitation
                </label>
                <input
                    type="password"
                    id="password"
                    bind:value={password}
                    class="w-full px-4 py-2 border rounded-lg focus:ring-2 focus:ring-wedding-primary focus:border-transparent"
                    placeholder="Enter password"
                    required
                />
            </div>

            {#if error}
                <p class="text-red-500 text-sm text-center">{error}</p>
            {/if}

            <button
                type="submit"
                class="w-full bg-wedding-primary text-white py-2 px-4 rounded-lg hover:opacity-90 transition-opacity"
            >
                Enter Site
            </button>
        </form>
    </div>
</div>

<style>
    :global(body) {
        background-color: var(--wedding-background, #fffaed);
    }
</style>
