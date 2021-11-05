<script>
  const id = $$props.id;

  $: classes = `tab-content ${$$props.class ? $$props.class : ''}`;
  $: style = $$props.style ? $$props.style : '';
</script>

<div class="{classes}" {id} {style}>
  <slot></slot>
</div>