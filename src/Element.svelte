<script>
  export let parent
  export let name
  export let elemId
  export let handleItemClick
  export let handleButtonClick
  export let key
</script>

<style>
  .componentItem {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #3e4c59;
    color: #eee;
    padding: 2px 10px;
    margin: 10px;
    border: 1px solid rgb(115, 117, 126);
    border-radius: 6px;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif,
      sans-serif;
    font-size: 1.5em;
    /* border: 2px solid brown; */
    cursor: pointer;
    margin-left: var(--leftMargin, 4rem);
    min-width: 60%;
    width: 260px;
  }
  .showBtn {
    border-radius: 20px 20px;
    background-color: orange;
    cursor: pointer;
    color: black;
  }
  p {
    letter-spacing: 0.75px;
  }
</style>

<div class="componentItem" on:click={() => handleItemClick()}>
  <p>{name}</p>
  <button
    class="showBtn"
    on:click|stopPropagation={(key) => handleButtonClick(key)}>
    +
  </button>
</div>
