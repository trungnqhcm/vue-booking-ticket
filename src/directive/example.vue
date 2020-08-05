<template>
  <div class="container">
    <h3 class="title">Example Directive</h3>
    <div class="row">
      <div class="col-sm-5">
        <div class="form-group">
          <label>Ma SP</label>
          <input type="text" class="form-control" ref="ma" />
        </div>
        <div class="form-group">
          <label>Ten SP</label>
          <input type="text" class="form-control" ref="ten" />
        </div>
        <div class="form-group">
          <label>Gia SP</label>
          <input type="text" class="form-control" ref="gia" />
        </div>
        <button
          class="btn btn-success"
          @click="addProduct($refs.ma.value, $refs.ten.value, $refs.gia.value)"
        >Them SP</button>
      </div>
    </div>
    <div class="row">
      <table class="table">
        <thead>
          <tr>
            <th>Ma</th>
            <th>Ten</th>
            <th>Gia</th>
          </tr>
        </thead>
        <tbody>
          <template v-if="listProduct && listProduct.length > 0">
            <tr
              v-for="(product, index) in listProduct"
              :key="product.id"
              :class="{'bg': index % 2 === 0}"
            >
              <td>{{product.id}}</td>
              <td>{{product.name}}</td>
              <td>{{product.price}}</td>
            </tr>
          </template>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      listProduct: []
    };
  },
  methods: {
    addProduct(id, name, price) {
      this.listProduct.push({ id, name, price });
    }
  }
};
</script>

<style>
.bg {
  background-color: aqua;
}
</style>