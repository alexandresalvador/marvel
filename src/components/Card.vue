<template>
<div class="card" style="width: 18rem;">
  <img :src="personagem.photo" class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">{{personagem.name}}</h5>
    <p class="card-text">{{personagem.about}}</p>
    <a href="#" class="btn btn-primary">Preview</a>
  </div>
</div>
</template>

<script>
export default {
  name: 'Card',
  props: {
      personagem: {
          required: true,
      },
  }
};
</script>


