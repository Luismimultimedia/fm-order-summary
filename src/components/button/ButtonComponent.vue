<template>
  <button
    :class="`button-${type}`"
  >
    {{ text }}
  </button>
</template>

<script>
export default {
    name: "ButtonComponent",
    props: {
        text: String,
        type: String,
    }
}
</script>

<style lang="scss">
    button {
        border: none;
        padding: 1rem;
        font-size: 1rem;
        font-weight: bold;
        margin-top: 1rem;
    }
    .button {
        &-primary {
            background-color: var(--color-bright-blue);
            color: var(--color-very-pale-blue);
            border-radius: 10px;
        }
        &-secondary {
            background-color: white;
            color: var(--color-desaturated-blue);
        } 
    }
</style>