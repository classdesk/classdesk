<script lang="ts">
  import Star from '~icons/lucide/star'

  import Dices from '~icons/lucide/dices'

  import ToolCard from '../components/ToolCard.svelte'
  import SmallToolCard from '../components/SmallToolCard.svelte'
</script>

<div class="flex flex-col max-h-screen h-screen p-10 mx-auto max-w-[1080px] 2xl:max-w-[1450px] shrink-0 gap-5">
  <nav class="flex items-center justify-between">
    <h1 class="font-mono text-4xl font-bold">
      <span class="text-primary">Class</span><span>Desk</span>
    </h1>
    <span class="font-mono text-neutral">dev.1</span>
  </nav>
  <div class="flex max-h-full py-5">
    <main class="flex flex-col max-w-full gap-8 grow">
      <article>
        <h2 class="flex items-center gap-1 pb-2 pl-2 text-lg font-medium">
          <Star />즐겨찾기
        </h2>
        <ul class="flex flex-wrap max-w-full gap-2">
          {#each Array(10) as _}
            <SmallToolCard Icon={Dices} color="#ffc107" name="도구 이름" url="/" />
          {/each}
        </ul>
      </article>
      <article>
        <h2 class="flex items-center gap-1 pb-2 pl-2 text-lg font-medium">
          <Star />최근 사용
        </h2>
        <ul class="flex flex-wrap max-w-full gap-3">
          {#each Array(10) as _}
            <ToolCard Icon={Dices} color="#ffc107" name="도구 이름" url="/" />
          {/each}
        </ul>
      </article>
    </main>
    <aside class="w-[400px] shrink-0 p-5 pb-0 bg-base-200 flex flex-col max-h-full h-full rounded-2xl gap-5 ml-3">
      <input type="text" class="input shrink-0" placeholder="도구 검색" />
      <div class="max-h-full overflow-y-auto">
        <ul class="grid grid-cols-2 gap-3">
          {#each Array(100) as _}
            <ToolCard Icon={Dices} color="#ffc107" name="도구 이름" url="/" />
          {/each}
        </ul>
      </div>
    </aside>
  </div>
</div>
