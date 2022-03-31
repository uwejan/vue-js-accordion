<template>
  <div>
    <div class="accordion" :class="{ 'accordion-flush' : flush === true}" :id="id">
      <div v-for="(item, i) in items" :key="item.id" class="accordion-item">
        <h2 class="accordion-header" :id="`heading${item.id}`">
          <button
              class="accordion-button"
              :class="{ collapsed: i > 0 }"
              type="button"
              data-bs-toggle="collapse"
              :data-bs-target="`#collapse${item.id}`"
              :aria-expanded="i === 0"
              :aria-controls="`collapse${item.id}`"
          >
            {{ item.title }}
          </button>
        </h2>
        <div
            :id="`collapse${item.id}`"
            class="accordion-collapse collapse"
            :class="{ show: i === 0 && alwaysOpen === true }"
            :aria-labelledby="`heading${item.id}`"
            :data-bs-parent="id"
        >
          <div class="accordion-body">
            {{ item.body }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Accordion",
  props:{
    id: {
      type: String,
      default: null
    },
    flush: {
      type: Boolean,
      default: false
    } ,
    alwaysOpen: {
      type: Boolean,
      default: true
    } ,
    items: Array,
  },
}
</script>


<style scoped>


</style>
