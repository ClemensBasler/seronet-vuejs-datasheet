<template>
<v-app>
  <Actionbar :componentId="componentId" @update="handleClickInParent" />
  <Datasheet color="pink" :componentId="componentId" :sections="sections" />
</v-app>
</template>

<script>
import Datasheet from './components/Datasheet'
import Actionbar from './components/Actionbar'

export default {
  components: {
    Datasheet,
    Actionbar
  },
  data() {
    return {
      componentId: "http://servicerobotik-ulm.de/ComponentsAndSystems#SmartCdlServer",
      sections: []
    }
  },
  methods: {
    handleClickInParent(sections, componentId) {
      this.sections = sections,
      this.componentId = componentId
    }
  }
}
</script>
