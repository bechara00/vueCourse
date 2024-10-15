<template>
  <h1 :class="$style['m-class']">
    Using module CSS with $ syntax (kabab-case)
  </h1>
  <h1 :class="$style.anotherStyle">
    Using module CSS with $ syntax (camel-case)
  </h1>
</template>

<style module>
/* kabab-case */
.m-class {
  background: firebrick;
  color: white;
}
.anotherStyle {
  background-color: blueviolet;
  color: white;
}
</style>
