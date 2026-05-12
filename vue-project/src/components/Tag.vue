<script lang="ts">
export default {
  name: 'Tag',
  props: {
    texto: { type: String, required: true },
    ativa: { type: Boolean }
  }
}
</script>

<template>
    <span class="tag" :class="{ ativa }">
        {{ texto }}
    </span>
</template>

<style scoped>
.tag {
  display: inline-block;
  border-radius: 0.5rem;
  min-width: 4.25rem;
  padding: 0.5rem;
  text-align: center;
  transition: 0.2s;
  color: var(--cinza, #444);
  background:var(--cinza-claro, #4e4d4d); ;
  font-weight: 00;
}

.tag.ativa{
  color: var(--creme, #FFFAF3);
  background: var(--coral, #F0633C);
  font-weight: 700;
}
</style>