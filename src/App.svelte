<style>
  h1,
  h2 {
    text-align: center;
  }
  h2 {
    margin-top: 20px;
  }
  #tip {
    width: 100%;
  }
  button {
    width: 100%;
  }
</style>

<div class="container">
  <div class="row">
    <div class="column">
      <h1>Tip Calculator</h1>
    </div>
  </div>
  <div class="row">
    <div class="column">
      <label for="bill">Bill</label>
      <input type="number" id="bill" min="0" />
    </div>
  </div>
  <div class="row">
    <div class="column">
      <label for="tip">Tip (15%)</label>
      <input type="range" id="tip" step="1" min="0" max="100" />
    </div>
  </div>
  <div class="row">
    <div class="column"><button class="button"> 15% </button></div>
    <div class="column">
      <button class="button button-outline"> 25% </button>
    </div>
    <div class="column">
      <button class="button button-outline"> 30% </button>
    </div>
  </div>
  <div class="row">
    <div class="column">
      <h2>Calculated Tip: $5.20</h2>
    </div>
  </div>
</div>
