<script>
  const id = $$props.id;

  $: classes = `nav nav-tabs ${$$props.class ? $$props.class : ''}`;
  $: style = $$props.style ? $$props.style : '';
</script>

<ul class={classes} {id} {style} role="tablist">
  <slot></slot>
</ul>