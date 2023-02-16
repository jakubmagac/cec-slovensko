<template>
  <div class="py-16">
    <h1>Workshops</h1>
    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aliquam nihil voluptas autem ipsam pariatur dolorum corrupti! Quaerat rem magnam illo reiciendis tenetur alias. Consequuntur temporibus harum laudantium modi dolorum? Nesciunt.</p>
    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aliquam nihil voluptas autem ipsam pariatur dolorum corrupti! Quaerat rem magnam illo reiciendis tenetur alias. Consequuntur temporibus harum laudantium modi dolorum? Nesciunt.</p>
    <div class="flip-card">
      <div class="flip-card-inner">
        <div class="flip-card-front">
          <img src="janosik_logo.jpg" alt="Avatar" style="width:300px;height:300px;">
        </div>
        <div class="flip-card-back">
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aspernatur, sequi? Tempora doloribus possimus velit corporis veniam cupiditate? Debitis quo nam, error eius iste, consectetur culpa repellat odit reprehenderit quisquam deleniti.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'WorkshopPage'
}
</script>

<style>
.flip-card {
  background-color: transparent;
  width: 300px;
  height: 200px;
  border: 1px solid #f1f1f1;
  perspective: 1000px; /* Remove this if you don't want the 3D effect */
  cursor: pointer;
}

/* This container is needed to position the front and back side */
.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.8s;
  transform-style: preserve-3d;
}
/* Do an horizontal flip when you move the mouse over the flip box container */
.flip-card:hover .flip-card-inner {
  transform: rotateY(180deg);
}

/* Position the front and back side */
.flip-card-front, .flip-card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden; /* Safari */
  backface-visibility: hidden;
}

/* Style the front side (fallback if image is missing) */
.flip-card-front {
  background-color: #bbb;
  color: #0c0c0c;
}

/* Style the back side */
.flip-card-back {
  background-color: #f2c4e3;
  color: #0c0c0c;
  width: 300px;
  height: 300px;
  display: flex;
  align-items: center;
  padding: 1em;
  transform: rotateY(180deg);
}
</style>
