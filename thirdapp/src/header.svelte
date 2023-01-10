<script>

</script>

<main>
    <div class="menuribbon.css">
        <button class="menubutton">Home</button>
        <select class="dropdownbutton">
          <option>Category</option>
          <option>Horror Movies</option>
          <option>Adventure</option>
          <option>Action</option>
        </select>
        <!-- <th>Movies</th> -->
        <button class="menubutton">Mylist</button>
        </div>
</main>

<style>
.menuribbon{
  display: flex;
  flex-direction: row;
  width:100%;
  background-color:rgba(247, 55, 55, 0.988) ;
}

.dropdownbutton{
  background-color:rgba(247, 55, 55, 0.988);
  font-size: 30px;
  border: 80px red;
  text-align: center;
  width:220px;
  /* text-decoration: none;  */
  /* display: inline-block; */
  padding: 10px 25px;
  transition: width 3s, height 3s;
  opacity: 95%;
  font-weight: bold;
}
.dropdownbutton:hover{
  text-align: center;
  align-items: center;
  opacity:100%;
  width:300px;
  height:100px;
  background-color: yellow;
}
.menubutton{
  background-color:rgba(247, 55, 55, 0.988);
  font-size: 25px;
  border: 20px black;
  text-align: center;
  width:150px;
  /* text-decoration: none;  */
  /* display: inline-block; */
  padding: 10px 25px;
  transition: width 3s, height 3s;
  opacity: 95%;
  font-weight: bold;
}
.menubutton:hover{
  text-align: center;
  align-items: center;
  opacity:100%;
  width:300px;
  height:100px;
  background-color: yellow;
}

</style>