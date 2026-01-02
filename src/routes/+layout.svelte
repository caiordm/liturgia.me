<script>
    import { dev } from "$app/environment";
    import { inject } from "@vercel/analytics";
    import { injectSpeedInsights } from '@vercel/speed-insights/sveltekit';

    inject({ mode: dev ? "development" : "production" });
    injectSpeedInsights();
    import "../app.css";
</script>

<slot />

<style>
    @import url("https://fonts.googleapis.com/css2?family=Kalnia:wght@100..700&display=swap");
    @import url("https://fonts.googleapis.com/css2?family=PT+Serif:ital,wght@0,400;0,700;1,400;1,700&display=swap");

    :global(html) {
        scroll-behavior: smooth;
        transition: 1s ease;
        overflow-x: hidden;
    }

    :global(body) {
        font-family: "Kalnia", serif;
        padding: 0;
        margin: 0;
        box-sizing: border-box;
    }

    :global(p) {
        font-family: "Playfair Display", serif;
    }
</style>
