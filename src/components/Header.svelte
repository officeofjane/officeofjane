<script>
  import { page } from '$app/state';

  const navItems = [
    { href: '/about', label: 'About' },
  ];
</script>

<header>
  <a class="home" href="/">officeofjane</a>
  <nav>
    {#each navItems as item}
      <a href={item.href}
      class:active={page.url.pathname === item.href} >
        {item.label}
      </a>
    {/each}
    <span>Notes</span>
  </nav>
</header>

<style>
  header {
    max-width: var(--copy-width);
    margin: 1% auto 0 auto;
    position: relative;

    display: flex;
    justify-content: space-between;
    align-items: center;

    font-size: 1rem;
  }

  header a {
    text-decoration: none;
  }

  header .home {
    font-family: monospace;
    font-size: 0.875rem;
  }

  header nav {
    display: flex;
    align-items: center;
    gap: clamp(1rem, 3vw, 2rem);
    margin: 0;
    padding: 0;
  }

  header nav a.active {
    color: var(--colour-highlight)
  }

  header nav span {
    color: #888;
  }
</style>