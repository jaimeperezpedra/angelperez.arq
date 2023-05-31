<!-- __layout.svelte -->
<script>
  import { Router, Route } from '@sveltejs/kit';

  import Home from './+page.svelte';
  import Works from './works/+page.svelte';
</script>

<Router>
  <Route path="/" component={Home} />
  <Route path="/works" component={Works} />
</Router>
