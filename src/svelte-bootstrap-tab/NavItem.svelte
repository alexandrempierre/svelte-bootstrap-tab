<script>
  const id = $$props.id;
  
  $: classes = `nav-item ${$$props.class ? $$props.class : ''}`;
  $: style = $$props.style ? $$props.style : '';
</script>

<li class={classes} {id} {style} role="presentation">
  <slot></slot>
</li>