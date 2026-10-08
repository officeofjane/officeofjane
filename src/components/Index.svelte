<script>
  import { getContext } from "svelte";
  import List from '$components/List.svelte';

  const copy = getContext("copy");
</script>

  <section id="bio">
    <h1>{copy.hed}</h1>
    <p>{copy.bio}</p>
  </section>

  <section id="grid">
    <div class=""><img alt="" src="./img/resilience.jpg"/></div>
    <div class=""><img alt="" src="./img/breastcancer.jpg"/></div>
    <div class=""><img alt="" src="./img/medals.jpg"/></div>  
    <div class=""><img alt="" src="./img/buzzwords.jpg"/></div>
    <div class=""><img alt="" src="./img/holidaychill.jpg"/></div>
  </section>

  <section>
    <h2>Selected projects</h2>
    <List data={copy.projects} />
  </section>

<style>
  section {
    max-width: var(--copy-width);
    margin: 0 auto;
    margin-bottom: var(--section-padding);
  }

  section:last-of-type {
    margin-bottom: calc(var(--section-padding) * 2);
  }

  h2 {
    font-size: 1.25rem;
  }

  p {
    width: 100%;
    text-wrap: pretty;

    font-size: 1.125rem;
  }

  #bio {
    margin-top: var(--section-padding);

    p {
      font-size: clamp(1.125rem, 3.25vw, 1.5rem);
    }
  }

  #grid {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    filter: var(--shadow-elevation-high);

    div {
      min-width: 100px;
      flex: 1;
      aspect-ratio: 1 / 1;
      padding: 4px;
      background-color: white;
      border: 1px solid var(--colour-background);
      border-radius: 6px; 
      outline: 2px solid white;
      overflow: hidden;
      box-shadow: var(--shadow-elevation-medium);
    }

    img {
      width: 100%;
      object-fit: cover;
    }
  }
</style>
