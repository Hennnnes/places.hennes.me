<script>
	export let src = '';
	export let title = '';
</script>

<div class="place">
	<img {src} alt="{title}" class="place__image">
	<h3 class="place__title">{title}</h3>
</div>

<style>
.place {
  overflow: hidden;
  position: relative;
}

.place:after {
  display: block;
  content: "";
  bottom: 0;
  position: absolute;
  left: 0;
  right: 0;
  background: rgba(255, 255, 255, 0.7);
  height: 45px;
}

.place__image {
  border-radius: 20px;
  width: 100%;
}

.place__title {
  color: #49504b;
  position: absolute;
  bottom: 15px;
  left: 15px;
  margin: 0;
  font-size: 1rem;
  text-shadow: 0px 0px 4px #fff;
  z-index: 1;
}
</style>