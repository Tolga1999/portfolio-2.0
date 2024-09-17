<template>
    <header>
        <ul>
            <li>
                <NuxtLink to="/">Home</NuxtLink>
            </li>
            <li><a href="https://www.linkedin.com/in/tolga-doganer-1b76aa161/"><img src="/assets/icons/linkedinLogo.svg"
                        alt="LinkedIn logo">
                </a>
            </li>
            <li>
                <a href="https://github.com/Tolga1999"><img src="/assets/icons/githubLogo.svg" alt="Github logo">
                </a>
            </li>
        </ul>
    </header>
</template>

<style>
header ul {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-grow: 1;
    width: 100%;
}

ul {
    list-style-type: none;
}

ul li:nth-of-type(1) {
    flex-grow: 1;
    font-size: 1.5em;
}

ul li a:nth-of-type(1) {
    color: var(--primary-color);
    font-weight: 500;
    text-decoration: none;
}

ul li:nth-of-type(2) {
    margin-right: 1.25em;
}

ul li a {
    display: flex;
    align-items: center;
}
</style>