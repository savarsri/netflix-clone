<script>
    export let value;
    export let handleClick;
    function disableBtn()
     {
      document.getElementById("myBtn").disabled = true
      }
</script>

<!-- <button class="square" on:click={increment}> {value} </button>   -->
<button id="myBtn" class="square" on:click={handleClick}>{value || ""}</button>

<style>
    .square {
        flex: 1 0 25%;
        width: 50px;
        height: 70px;
        color: blue;
        background-color: whitesmoke;
        border: 2px solid black;
        margin: 5px;
        padding: 5px;
        font-size: 50px;
        text-align: center;
    }

    .square:hover {
        border: 2px solid red;
    }
</style>
