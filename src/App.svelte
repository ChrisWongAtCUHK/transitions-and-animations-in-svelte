<script>
  import ElasticOut from './ElasticOut.svelte';
  import Fade from './Fade.svelte';
  import Tabs from './Tabs.svelte';

  // List of tab items with labels, values and assigned components
  let items = [
    { label: 'Elastic Out',
     value: 1,
     component: ElasticOut
    },
    { label: 'Fade',
     value: 2,
     component: Fade
    }
  ];
</script>

<Tabs {items} />