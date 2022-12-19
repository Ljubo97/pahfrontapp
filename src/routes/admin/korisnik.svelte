<script>
export let name="Ime korisnika";
export let opis ="Opis korisnika";
</script>



<div class="card">
   
    <div class="container">
      <h4>{name}</h4>
      <p>{opis}</p>
    </div>
  </div>

  <style>
.card {
  /* Add shadows to create the "card" effect */
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
}

/* On mouse-over, add a deeper shadow */
.card:hover {
  background-color: blueviolet;

  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}

/* Add some padding inside the card container */
.container {
  padding: 2px 16px;
}

  </style>