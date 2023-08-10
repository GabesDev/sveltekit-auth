<script lang="ts">
  import { page } from "$app/stores"
</script>

<h1>Admin</h1>

{#if $page.data.user}
  <p>Hello {$page.data.user.name}</p>
{/if}

{#if $page.data.user.role === "ADMIN"}
  <form action="/logout" method="post">
    <button type="submit">Log Out</button>
  </form>
{/if}
