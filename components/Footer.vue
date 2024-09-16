<template>
    <footer>
        <h2>Get in touch</h2>
        <span>tolgadoganer@outlook.com</span>
        <div class="links-container">
            <a><img src="/assets/icons/linkedinLogoWhite.svg" alt="linkedIn logo">Linkedin</a>
            <a><img src="/assets/icons/githubLogoWhite.svg" alt="github logo">Github</a>
        </div>
    </footer>
</template>

<style scoped>
footer{
    background-color: var(--primary-color);
    padding: 2.5em;
    padding-top: 3.5em;
    margin-top: 4em;
}

h2, span{
    color: var(--secondary-color);
    font-size: 2.5em;
    font-weight: 500;
}

span{
    display: inline-block;
    margin-top: 0.5em;
    font-size: 1.25em;
}

.links-container, a{
    display: flex;
    align-items: center;
    gap: 1em;
}

.links-container{
    margin-top: 3em;
}

a{
    color: var(--secondary-color);
    padding: 0.5em 1.25em;
    border: 1px solid var(--secondary-color);
    border-radius: 0.5em;
    gap: 0.5em;
    font-weight: 500;
}
</style>