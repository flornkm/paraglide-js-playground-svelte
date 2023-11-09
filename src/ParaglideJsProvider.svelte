<script>
  import { languageTag, onSetLanguageTag } from "./paraglide/runtime"

  // initialize the language tag
  $: _languageTag = languageTag

  onSetLanguageTag((newLanguageTag) => {
    _languageTag = newLanguageTag
  })
</script>

{#key _languageTag}
  <slot />
{/key}
