<script>
  import { setLanguageTag, languageTag } from "./paraglide/runtime"
  import * as m from "./paraglide/messages"
  import ParaglideSvelte from "./ParaglideJsProvider.svelte"
</script>

<ParaglideSvelte>
  <p>{m.greeting({ name: "Samuel", count: 5 })}</p>
  <p>{m.currentLanguageTag({ languageTag })}</p>
  <button on:click={() => setLanguageTag("de")}>change language to "de"</button>
  <button on:click={() => setLanguageTag("en")}>change language to "en"</button>
</ParaglideSvelte>
