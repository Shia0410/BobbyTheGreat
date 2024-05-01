<template>
  <div class="gallery" >
    <div v-for="image in images" :key="image.id" class="gallery-item" align="center">
      <img :src="image.url" :alt="image.alt" class="gallery-image">
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: [
        { id: 1, url: 'path/to/image1.jpg', alt: 'Image 1' },
        { id: 2, url: 'path/to/image2.jpg', alt: 'Image 2' },
        { id: 3, url: 'path/to/image3.jpg', alt: 'Image 3' },
        // Add more images here
      ]
    };
  }
};
</script>

<style scoped>
.gallery {
  margin: 20px;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 2fr)); /* Updated property */
  grid-gap: 20px;
}

.gallery-item {
  position: relative;
  overflow: hidden;
  border-radius: 10px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  width: 300px; /* Set a fixed width */
  height: 300px; /* Set a fixed height */
}

.gallery-item:hover .gallery-image {
  transform: scale(1.1);
}
</style>
