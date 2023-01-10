<script>
  import Question from "./question.svelte";
  import Option1 from "./options.svelte";
  import Option2 from "./options.svelte";
  let a;

  const pkg = [
    { question:"________DDL command is used to change the structure of a database.",},
    { option1: "Apple", option2: "Banana" },
    { question: "Which key helps to run a query?" },
    { option1: "cat", option2: "dog" },
    { question: "How many sections are there in a Query Design window?" },
    { option1: "elephant", option2: "fruit" },
    { question: "Which key defines a relationship between two tables?" },
    { option1: "gun", option2: "house" },
    { question: "What does the top section of a query window display?" },
    { option1: "ikigai", option2: "just" },
    { question: "A query can be previewed by pressing." },
    { option1: "katana", option2: "lion" },
  ];

  // const pkg2 = [
  // ];
  let i = 0;
  let j=1;
  function increment() {
    i=i+2;
    j=j+2;
  }
</script>

<!-- <Counter {...pkg}/> -->
<main class="fullscreen">
  <div class="intro">
    <p>COMMON QUIZ</p>
  </div>

  <Question {...pkg[i]}/>
  <div class= "option-alignment">
  <Option1 {...pkg[j]} />
  </div>
 
  <div class="button">
    <button>Evaluate</button>
    <button on:click={increment}>Submit</button>
  </div>
</main>

<style>
  /* body{
    padding: 0;
    margin: 0;
        
    background-color: green;
}  */
  .intro {
    margin: 3% 0%;
    display: flex;
    width: 100%;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: blue;
    background-color: aliceblue;
  }
  .fullscreen {
    background-color: aqua;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    overflow: auto;
    display: flex;
    flex-direction: column;
    justify-content: top;
    align-items: center;
    text-align: left;}

  .button{
    margin-top: 10%;
    display: flex;
    flex-direction: row;
    width: 30%;
    padding: 0% 5%;
    background-color: bisque;
    justify-content: space-between;
  }

  .button > button {
    font-size: 30px;
  }

  .option-alignment{
    padding-top: 8%;
    display: flex;
    flex-direction: column;
   
  }
</style>
