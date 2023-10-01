<script lang="ts">
  export let Icon: any
  export let color: string
  export let name: string
  export let url: string
</script>

<li>
  <a href={url} class="border-0 rounded-full btn" style="background: {color}">
    <Icon class="w-6 h-6" />
    <span class="text-lg">{name}</span>
  </a>
</li>
