<template>
    <main>
        <Header />
        <section class="call-to-action-container">
            <span>-- Hi I'm Tolga</span>
            <h1>Frontend Developer</h1>
            <p>
                Hello! My name is Tolga, I’m 24 years old and I like to design and code projects in Vue.js, Sveltekit and
                Nuxt.js. I recently graduated at the Amsterdam University of Applied Sciences! 🎉
            </p>
            <a href="/">Contact</a>
        </section>

        <section class="project-container">
            <h2>My projects</h2>
            <Project />
        </section>
    </main>
    <Footer />
</template>

<style>
.call-to-action-container {
    margin: 3.875em 0 4.75em 0;
}

.call-to-action-container p{
    line-height: 2em;
    margin-bottom: 0.75em;
    font-size: 1.25em;
}

span{
    color: var(--tertiary-text-color);
    font-weight: 500;
}

/* styling for section anchors */
section a{
    display: inline-block;
    color: var(--secondary-color);
    background-color: var(--primary-color);
    padding: 0.75em 2.25em;
    border-radius: 0.5em;
    text-decoration: none;
}

/* projects */
.project-container h2{
    margin-bottom: 0.5em;
}
</style>