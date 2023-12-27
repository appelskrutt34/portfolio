<script>
    import "../app.css";
    import Nav from "$lib/components/Nav.svelte"
  </script>
  
  <div class="bg-neutral-900 text-neutral-50 font-primary">
    <Nav></Nav>
    <slot />
  </div>
