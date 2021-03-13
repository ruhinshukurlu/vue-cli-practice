<template>
    <div class="col-4">
        <div class="card" style="width: 18rem;">
            <img :src="url" class="card-img-top" alt="...">
            <div class="card-body">
                <h5 class="card-title">{{ item }}</h5>
                <p class="card-text">{{desc}}</p>
                <div class="d-flex align-items-center justify-content-center quantity-box">
                    <button class="count-btn" @click="counter > 0 ? (counter -= 1) : 0">-</button>
                        <span class="quant-text m-2">Quantity: {{ counter }}</span>
                    <button class="count-btn" @click="counter += 1">+</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  props: ["item", "url", 'desc'],
  data() {
    return {
      counter: 0,
    };
  }
};
</script>

<style scoped>
    .count-btn{
        width: 40px;
        height: 40px;
        background-color: rgb(241, 231, 231);
        border-radius: 50%;
        border: none;
    }

    .quantity-box{
        border: 1px solid #ccc;
        padding: 5px;
        border-radius: 10px;
    }

</style>