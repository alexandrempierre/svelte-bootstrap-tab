<script>
  import { setContext } from 'svelte';
  import { writable } from "svelte/store";

  const activeTabId = writable('');

  setContext('tabComponent', {
    activeTabId,
    setActiveTabId: (tabId) => {
      activeTabId.set(tabId);
    }
  });
</script>

<div {...$$restProps}>
  <slot name="nav-tabs"></slot>
  <slot name="tab-content"></slot>
</div>