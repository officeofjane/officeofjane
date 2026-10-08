<script>
  let { data } = $props();
</script>

<ul>
  {#each data as { item, link, desc, detail }}
    <li>
      <div>
        {#if link}
          <a class="item" href={link}>{item}</a>
        {:else}
          {item}
        {/if}
        <span class="desc dim">{desc}</span>
      </div>
      <div class="detail dim">{detail}</div>
    </li>
  {/each}
</ul>

<style>
  ul {
    width: 100%;
    padding: 0;
    list-style: none;

    --color-text-dim: ##2d5a3d;
    --color-border: #d0d6d4;
  }

  li {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    gap: 8px;
    
    padding: 8px 0;
    border-bottom: 1px solid var(--colour-border);

    line-height: 1.5;
  }

  .desc {
    display: block;
    font-size: 0.875rem;
  }

  .detail {
    min-width: 3.75rem;
    font-family: var(--font-mono);
    font-size: 0.75rem;
    text-align: right;
  }

  .dim {
    color: var(--colour-text-dim);
  }
</style>