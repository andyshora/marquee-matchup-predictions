<template>
  <div class="fixture">
    <Badge :team="home"></Badge>
    <Badge :team="away"></Badge>
  </div>
</template>

<script>
import Badge from 'components/badge';

export default {
  name: 'Fixture',
  props: ['home', 'away'],
  components: { Badge }
}
</script>

<style>
.fixture {
  padding: 10px;

  display: flex;
  align-items: center;
  justify-content: center;

  text-align: center;
}
.fixture::after {
  content: 'v';
  position: absolute;
  font-size: 20px;
}

.fixture > .badge {
  margin: 0 50px;

  animation: spinIn 1s forwards;
  transform: rotateY(-90deg);
}

@keyframes spinIn {
  0% {
    transform: rotateY(-90deg);
  }
  100% {
    transform: rotateY(0deg);
  }
}
</style>
