<template>
  <v-btn-toggle
    :value="value"
    class="DataSelector"
    mandatory
    @change="$emit('input', $event)"
  >
    <v-btn
      v-ripple="false"
      value="confirmedTransition"
      class="DataSelector-Button"
    >
      Daily
    </v-btn>
    <v-btn v-ripple="false" value="cumulative" class="DataSelector-Button">
      Total
    </v-btn>
  </v-btn-toggle>
</template>

<style lang="scss">
.DataSelector {
  margin-top: 2px;
  border: 1px solid $gray-4;
  background-color: $white-1;
  &-Button {
    border: none !important;
    margin: 2px;
    border-radius: 4px !important;
    height: 24px !important;
    font-size: 12px !important;
    color: $gray-1 !important;
    background-color: $white-1 !important;
    &::before {
      background-color: inherit;
    }
  }

  & .v-btn--active {
    background-color: $purple-2 !important;
    color: $white-1 !important;
  }
}
</style>

<script>
export default {
  name: 'DataSelector',
  props: {
    value: {
      type: String,
      required: false,
      default: ''
    }
  }
}
</script>
