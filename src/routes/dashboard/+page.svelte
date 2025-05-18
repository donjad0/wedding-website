<script lang="ts">
    import { onMount } from 'svelte';
    
    onMount(() => {
        // Simple check if user came from login
        // In a real app, you'd want proper session management
        if (!document.referrer.includes('/')) {
            window.location.href = '/';
        }
    });
</script>

<div class="container py-16">
    <h1 class="animate-fade-in">
        Joe & Jade
    </h1>

    <div class="animate-fade-in-delay-2 text-center mt-8 navbar">
        <a href="/dashboard" class="mx-8 hover:text-wedding-primary transition-colors">Home</a>
        <a href="/photos" class="mx-8 hover:text-wedding-primary transition-colors">Schedule</a>
        <a href="/story" class="mx-8 hover:text-wedding-primary transition-colors">Information</a>
        <a href="/rsvp" class="mx-8 hover:text-wedding-primary transition-colors">RSVP</a>
    </div>

    <p class="animate-fade-in-delay-2 text-center text-xl mt-12">
        We're getting married!
    </p>
    
    <div class="animate-fade-in-delay-2 text-center mt-8">
        <p class="text-2xl">
            May 29th 2026
        </p>
    </div>

    <div class="animate-fade-in-delay-3 text-center mt-12 mb-24">
        <button class="btn btn-primary">
            RSVP Now
        </button>
    </div>
</div>

<style>
    .navbar {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 2rem;
        padding: 1rem 0;
    }

    .navbar a {
        font-size: 1.1rem;
        text-decoration: none;
    }

    button {
        transition: all 0.2s ease-in-out;
    }
    
    button:hover {
        transform: scale(1.05);
    }
    
    button:active {
        transform: scale(0.95);
    }
</style> 