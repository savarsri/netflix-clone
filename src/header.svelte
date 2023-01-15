<script>

</script>

<main>
    <div class="menuribbon">
        <button class="menubutton">Home</button>
        <select class="dropdownbutton">
          <option>Category</option>
          <option>Horror Movies</option>
          <option>Adventure</option>
          <option>Action</option>
        </select>
        <!-- <th>Movies</th> -->
        <button class="menubutton">Mylist</button>
        <button>Sign In</button>
    </div>

</main>

<style>
.menuribbon{
  display: flex;
  flex-direction: row;
  width:100%;
  /* background-color: black ; */
}

.dropdownbutton{

  font-size: 30px;
  border: 80px red; 
  text-align: center;
  width:220px;
  background-color: black;
  color:white;
  font-family: Bebas Neue;
  /* text-decoration: none;  */
  /* display: inline-block; */
  height: 120px;
  padding: 10px 25px;
  transition: width 3s, height 3s;
  /* opacity: 95%; */
  /* font-weight: bold; */
}
.dropdownbutton:hover{
  text-align: center;
  align-items: center;
  opacity:100%;
  width:300px;
  height:120px;
  background-color: yellow;
  font-family: Bebas Neue;
  color:red;
}
.menubutton{
  font-family: Bebas Neue;
  background-color: transparent;  
  color:white;
  font-size: 25px;
  border: 80px red; 
  text-align: center;
  width:150px;
  height: 120px;
  /* text-decoration: none;  */
  /* display: inline-block; */
  padding: 10px 25px;
  transition: width 3s, height 3s;
  /* opacity: 95%; */
  /* font-weight: bold; */
}
.menubutton:hover{
  color:red;
  text-align: center;
  align-items: center;
  /* opacity:100%; */
  width:300px;
  font-family: Bebas Neue;
  height:120px;
  background-color: yellow;
}
</style>