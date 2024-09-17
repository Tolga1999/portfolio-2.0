<script setup>
const QUERY = `
  query {
  calltoaction{
    smallText
    title
    paragraph
    contact
  }
    
  allProjects{
    title
    mockupImage {
      filename
      url
    }
    backgroundColor {
      hex
    }
    labels
    description
    linkToProject
  }
}
`;

const { data, error } = await useGraphqlQuery({ query: QUERY });
</script>

<template>
    <main>
        <Header />
        <section class="call-to-action-container">
            <span>-- {{ data.calltoaction.smallText }}</span>
            <h1>{{ data.calltoaction.title }}</h1>
            <p>{{ data.calltoaction.paragraph }}</p>
            <a :href="data.calltoaction.contact">Contact</a>
        </section>
            
        <h2 class="projects-h2">My projects</h2>
        <section class="projects-container">
            <Project v-for="project in data.allProjects" :title="project.title"
                :description="project.description" :url="project.mockupImage.url" 
                :backgroundColor="project.backgroundColor.hex" :linkProject="project.linkToProject" :labels="project.labels"/>
        </section>
    </main>
    <Footer />
</template>

<style>
.call-to-action-container {
    margin: 3.875em 0 4.75em 0;
    max-width: 40em;
}

.call-to-action-container p {
    line-height: 1.6em;
    margin-bottom: 0.75em;
    font-size: 1.25em;
}

span {
    color: var(--tertiary-text-color);
    font-weight: 500;
}

/* styling for section anchors */
section a {
    display: inline-block;
    color: var(--secondary-color);
    background-color: var(--primary-color);
    padding: 0.75em 2.25em;
    border-radius: 0.5em;
    text-decoration: none;
}

/* projects */
.projects-h2 {
    margin-bottom: 0.5em;
}

.projects-container{
    display: flex;
    flex-wrap: wrap;
    gap: 3.25em;
    flex-grow: 1;
  }

/* media queries for desktop */
@media screen and (min-width: 800px) {
  h1{
    font-size: 4em;
  }

  h2{
    font-size: 3em;
  }

  h3{
    font-size: 1.5em;
  }
}

@media screen and (min-width: 1300px) {
  main {
    margin-left: 14em;
    margin-right: 14em;
  }
}
</style>