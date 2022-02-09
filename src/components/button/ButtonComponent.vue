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
            box-shadow: 0px 5px 11px -2px rgba(99, 89, 209, 0.54);
            &:hover {
                opacity: .7;
            }
        }
        &-secondary {
            background-color: white;
            color: var(--color-desaturated-blue);
            &:hover {
                color: black;
            }
        } 
    }
</style>