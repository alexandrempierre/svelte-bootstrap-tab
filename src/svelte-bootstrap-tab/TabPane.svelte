<script>
  import { getContext } from "svelte";

  export let tabId;
  const { activeTabId } = getContext('tabComponent');

  $: tabOpen = $activeTabId === tabId;
  $: classes = `tab-pane fade ${tabOpen ? 'show active' : ''} ${$$props.class ? $$props.class : ''}`;
  $: style = $$props.style ? $$props.style : '';
</script>

<section 
        class={classes}
        id="{tabId}"
        role="tabpanel"
        aria-labelledby="{tabId}-tab"
        {style}>
  <slot></slot>
</section>