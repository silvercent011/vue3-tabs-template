<template>
<Tabs>
  <Tab :title="'TAB1'">
    <h2>Tab 1 Content</h2>
  </Tab>
  <Tab :title="'TAB2'">
    <h2>Tab 2 Content</h2>
  </Tab>
  <Tab :title="'TAB3'">
    <h2>Tab 3 Content</h2>
  </Tab>
  <Tab :title="'TAB4'">
    <h2>Tab 4 Content</h2>
  </Tab>
</Tabs>
</template>

<script>
import Tabs from "@/components/Tabs.vue";
import Tab from "@/components/Tab.vue";

export default {
    components: { Tabs, Tab }
}
</script>
