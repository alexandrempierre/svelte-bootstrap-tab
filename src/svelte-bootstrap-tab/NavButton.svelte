<script>
  import { getContext, onMount } from 'svelte';

  export let tabId, active = false;
  const { setActiveTabId, activeTabId } = getContext('tabComponent');

  onMount(() => {
    if (active || !$activeTabId) setActiveTabId(tabId);
  });

  $: tabOpen = $activeTabId === tabId;
  $: classes = `nav-link ${tabOpen ? 'active' : ''} ${$$props.class ? $$props.class : ''}`;
  $: style = $$props.style ? $$props.style : '';
</script>

<button
        class={classes}
        id="nav-{tabId}-tab" 
        data-bs-toggle="tab" 
        data-bs-target="#{tabId}" 
        type="button"
        role="tab" 
        aria-controls="nav-{tabId}" 
        aria-selected="{tabOpen}"
        {style}
        on:click={() => setActiveTabId(tabId)}>
  <slot></slot>
</button>