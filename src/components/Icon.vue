<template>
  <svg>
    <use :xlink:href="'#' + name"/>
  </svg>
</template>

<script lang="ts">
let importAll = (requireContext: any) => requireContext.keys().forEach(requireContext);
try{
  importAll(require.context('../assets/icons', true, /\.svg$/));
}catch (error){
  console.log(error);
}
export default {
  name: "Icon",
  props: ['name']
}
</script>

<style lang="scss" scoped>

</style>