<script setup>
defineProps({
  title: String,
  description: String,
  url: String,
  backgroundColor: String,
  linkProject: String,
  labels: Object,
});
</script>

<template>
    <section>
        <img :src="url" alt="Vervoerregio Amsterdam">
        <h3>{{ title }}</h3>
        <span v-for="label in labels">{{ label }}</span>
        <p>
            {{ description }}
        </p>
        <a :href=linkProject>See more</a>
    </section>
</template>

<style scoped>
img {
    padding: 0 1em;
    background-color: v-bind('backgroundColor');
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