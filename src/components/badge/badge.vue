<template>
  <div class="badge">
    <div class="badge__img"></div>
    <p>{{ team }}</p>
  </div>
</template>

<script>
export default {
  name: 'Badge',
  props: ['team']
}
</script>

<style>
.badge {
  padding: 10px;
}
.badge__img {
  display: block;
  width: 100px;
  height: 100px;
  background: white;
  border-radius: 50%;
  box-shadow: 3px 3px 5px rgba(0, 0, 0, 0.5);
}
.badge p {
  display: block;
  text-align: center;
}
</style>
