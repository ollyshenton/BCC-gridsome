<template>
    <a
      v-if="!disabled"
      :href="url"
      :class="`${variant} ${disabled}`"
      :disabled="disabled"
       class="button"
    >
      <span v-if="icon.length" class="button--icon">
        <slot name="svgContent"></slot>
      </span>
      <slot>{{ text }}</slot>
    </a>
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
    
  }
};
</script>

<style lang="scss" scoped>
.button,
button {
  color: $white;
  background: $black;
  padding: 14px 24px;
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
  &:hover {
    background-color: $lightgrey;
    color: $black;
  }
}
.button--icon {
  height: rem(18px);
}
.secondary {
  border: 3px solid grey;
  background-color: $lightgrey;
}
</style> 