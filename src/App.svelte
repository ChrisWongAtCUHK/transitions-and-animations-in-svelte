<script>
	import Tab1 from './ElasticOut.svelte';
  import Tabs from './Tabs.svelte';

  // List of tab items with labels, values and assigned components
  let items = [
    { label: 'Elastic Out',
		 value: 1,
		 component: Tab1
		}
  ];
</script>

<Tabs {items} />