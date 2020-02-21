<script>
  import { Router } from "@sveltech/routify";
  import { routes } from "@sveltech/routify/tmp/routes";

  function getTranslations(lang) {
    fetch('/static/lang.json')
            .then(result => result.json())
            .then(translation => console.log(translation));
  }

  getTranslations('en');
</script>

<Router {routes} />