<template>
    <div class="horizontal-line">
        <slot/>
    </div>
</template>

<style scoped>
.horizontal-line {
  overflow: hidden;
  text-align: center;
  margin: 1.5rem 24px 1.25rem 24px;
}

.horizontal-line:before,
.horizontal-line:after {
  background-color: #e2e8f0;
  content: "";
  display: inline-block;
  height: 1px;
  position: relative;
  vertical-align: middle;
  width: 50%;
}

.horizontal-line:before {
  right: 0.5em;
  margin-left: -50%;
}

.horizontal-line:after {
  left: 0.5em;
  margin-right: -50%;
}
</style>