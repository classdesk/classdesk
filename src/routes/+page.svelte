<script lang="ts">
  import Dices from '~icons/lucide/dices'

  import ToolCard from '../components/ToolCard.svelte'
</script>

<div class="flex flex-col max-h-screen h-screen p-10 mx-auto max-w-[1080px] 2xl:max-w-[1450px] shrink-0">
  <nav class="flex items-center justify-between">
    <h1 class="font-mono text-4xl font-bold">
      <span class="text-primary">Class</span><span>Desk</span>
    </h1>
    <span class="font-mono text-neutral">dev.1</span>
  </nav>
  <div class="flex max-h-full py-5">
    <main class="grow" />
    <aside class="w-[400px] p-5 pb-0 bg-base-200 flex flex-col max-h-full h-full rounded-2xl gap-5">
      <input type="text" class="input shrink-0" placeholder="도구 검색" />
      <div class="max-h-full overflow-y-auto">
        <ul class="grid grid-cols-2 gap-5">
          {#each Array(100) as _}
            <ToolCard Icon={Dices} color="#ffc107" name="도구 이름" url="/" />
          {/each}
        </ul>
      </div>
    </aside>
  </div>
</div>
