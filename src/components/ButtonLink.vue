<template>
  <div>
    <a
      v-if="!disabled"
      :href="url"
      :class="`${variant} ${disabled}`"
      :disabled="disabled"
    >
      <span v-if="icon.length" class="button--icon">
        <slot name="svgContent"></slot>
      </span>
      <slot>{{ text }}</slot>
    </a>
    <div
      v-else
      :class="`${variant}`"
      :disabled="disabled"
      class="disabled true"
      aria-label="disabled button"
    >
      <span v-if="icon.length" class="button--icon">
        <slot name="svgContent"></slot>
      </span>
      <slot>{{ text }}</slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "ButtonLink",
  props: {
    url: {
      type: String,
      default: "url"
    },
    text: {
      type: String,
      required: true,
      default: "Button"
    },
    variant: {
      type: String,
      default: "button"
    },
    icon: {
      type: String,
      required: false,
      default: "icon"
    },
    disabled: {
      type: Boolean,
      default: false
    }
  }
};
</script>

<style lang="scss" scoped>
.button,
button {
  color: $white;
  text-align: center;
  cursor: pointer;
  text-decoration: none;
  padding: rem(12.5px) rem(22px);
  font-size: $font-size-body;
  font-family: $font-family;
  font-weight: $font-weight-reg;
  display: inline-flex;
  line-height: 1.1;

  span {
    padding-right: rem(10px);
  }
  svg {
    fill: $white;
    height: rem(18px);
  }
}
.button--icon {
  height: rem(18px);
}
</style>