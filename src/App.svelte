<script>
  let bill = 10.25;
  let tip = 15;

  function calculatedTip(bill, tip) {
    const tipAmount = (tip / 100) * bill;
    return tipAmount.toLocaleString("en-US", {
      style: "currency",
      currency: "USD",
    });
  }

  function changeTip(newTip) {
    tip = newTip;
  }

  $: tipDisplay = calculatedTip(bill, tip);
</script>

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
      <input bind:value={bill} type="number" id="bill" min="0" />
    </div>
  </div>
  <div class="row">
    <div class="column">
      <label for="tip">Tip ({tip}%)</label>
      <input
        bind:value={tip}
        type="range"
        id="tip"
        step="1"
        min="0"
        max="100" />
    </div>
  </div>
  <div class="row">
    <div class="column">
      <button
        on:click={() => changeTip(15)}
        class:button-outline={tip !== 15}
        class="button">
        15%
      </button>
    </div>
    <div class="column">
      <button
        on:click={() => changeTip(25)}
        class:button-outline={tip !== 25}
        class="button">
        25%
      </button>
    </div>
    <div class="column">
      <button
        on:click={() => changeTip(30)}
        class="button"
        class:button-outline={tip !== 30}>
        30%
      </button>
    </div>
  </div>
  <div class="row">
    <div class="column">
      <h2>Calculated Tip: {tipDisplay}</h2>
    </div>
  </div>
</div>
