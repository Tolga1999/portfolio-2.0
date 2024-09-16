<template>
    <section>
        <img src="assets/images/vervoerregioAmsterdam.svg" alt="Vervoerregio Amsterdam">
        <h3>Toolgankelijkheid - Vervoerregio Amsterdam</h3>
        <span>Design</span>
        <span>Frontend</span>
        <p>
            Project for Vervoerregio Amsterdam focusing on WCAG guidelines and the specific check ups between their
            partners. This project is built with a unique design, Sveltekit, and Hygraph CMS.
        </p>
        <a href="/">See more</a>
    </section>
</template>

<style scoped>
img {
    padding: 0 1em;
    background-color: #DE0058;
    border-radius: 1em;
    width: 100%;
}

h3 {
    margin-top: 0.5em;
}

/* labels */
span {
    display: inline-block;
    color: var(--primary-color);
    background-color: var(--primary-label-color);
    border: 2px solid var(--secondary-label-color);
    border-radius: 1.5em;
    padding: 0.75em 2em;
    font-weight: 500;
    margin-right: 0.75em;
    margin-top: 1em;
}

p{
    color: var(--tertiary-text-color);
    line-height: 1.5em;
    margin: 1em 0;
}
</style>