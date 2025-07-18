<script lang="ts">
  import { Button } from '$lib/components/ui/button';
  import { SunIcon, MoonIcon } from '@lucide/svelte';
  import { toggleMode } from 'mode-watcher';
</script>

<Button
  class="absolute top-0 right-0 m-2 md:m-8"
  onclick={toggleMode}
  variant="outline"
  size="icon"
>
  <SunIcon
    size={20}
    class="absolute rotate-0 transition-all duration-200 dark:-rotate-90 dark:opacity-0"
  />
  <MoonIcon
    size={20}
    class="absolute rotate-90 opacity-0 transition-all duration-200 dark:rotate-0 dark:opacity-100"
  />
  <span class="sr-only">Toggle theme</span>
</Button>
