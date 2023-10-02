<script lang="ts">
  import Star from '~icons/lucide/Star'

  export let Icon: any
  export let color: string
  export let name: string
  export let url: string
</script>

<li>
  <a href={url} class="w-full h-24 px-3 pt-1 border-0 btn rounded-xl" style="background: {color}">
    <div class="flex justify-between w-full">
      <Icon class="w-6 h-6" />
      <button>
        <Star class="w-6 h-6" />
      </button>
    </div>
    <span class="w-full text-lg font-medium text-left">{name}</span>
  </a>
</li>
