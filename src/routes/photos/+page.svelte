<div class="container py-16">
    <h1 class="animate-fade-in text-center mb-12">Schedule</h1>

    <div class="max-w-2xl mx-auto animate-fade-in-delay-2">
        <div class="timeline-item mb-12">
            <h3 class="text-xl font-semibold mb-2">Ceremony</h3>
            <p class="text-lg mb-1">2:00 PM - 3:00 PM</p>
            <p class="text-gray-600">Join us as we exchange vows and celebrate our love.</p>
        </div>

        <div class="timeline-item mb-12">
            <h3 class="text-xl font-semibold mb-2">Cocktail Hour</h3>
            <p class="text-lg mb-1">3:00 PM - 4:00 PM</p>
            <p class="text-gray-600">Enjoy drinks and hors d'oeuvres while we take photos.</p>
        </div>

        <div class="timeline-item mb-12">
            <h3 class="text-xl font-semibold mb-2">Reception</h3>
            <p class="text-lg mb-1">4:00 PM - 10:00 PM</p>
            <p class="text-gray-600">Dinner, dancing, and celebrating!</p>
        </div>
    </div>
</div>

<style>
    .timeline-item {
        position: relative;
        padding-left: 2rem;
        border-left: 2px solid var(--wedding-primary);
    }

    .timeline-item::before {
        content: '';
        position: absolute;
        left: -0.5rem;
        top: 0.5rem;
        width: 1rem;
        height: 1rem;
        background-color: var(--wedding-primary);
        border-radius: 50%;
    }
</style> 