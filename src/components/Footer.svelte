<script>
  import { MailIcon } from 'svelte-feather-icons';
</script>

<footer>
  <div class="wrapper">© Handcoded with &#9829; in 2026. <a href="mailto:jane@officeofjane.com">Email me</a> <MailIcon size="13" /></div> 
</footer>

<style>
  footer {
    max-width: var(--copy-width);
    margin: 0 auto;
    padding: 8px 0px;

    display: flex;
    justify-content: center;
    text-align: center;

    color: var(--colour-primary);
    font-size: 0.75rem;
    font-family: var(--font-mono);
  }

  .wrapper {
    display: flex;
    gap: 8px;
    align-items: center;
  }
</style>