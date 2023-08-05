<template>
  <div>
    <select v-model="selectedValue">
      <option v-for="option in options" :key="option.value" :value="option.value">
        {{ option.label }}
      </option>
    </select>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedValue: null,
      options: [
        { value: 'option1', label: 'Option 1' },
        { value: 'option2', label: 'Option 2' },
        { value: 'option3', label: 'Option 3' },
      ],
    };
  },
  watch: {
    selectedValue(newValue) {
      // 親コンポーネントに選択した値を伝える
      this.$emit('selected', newValue);
    },
  },
};
</script>
