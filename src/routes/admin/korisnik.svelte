<script>
  import {createEventDispatcher} from 'svelte'
    import { claim_element } from 'svelte/internal';
export let name="Ime korisnika";
export let opis ="Opis korisnika";
export let prikazi=() => {};
export let prikazI=() => {alert(name)};

/**
     * @type {(arg0: string) => any}
     */
 export let imeKorisnika=() => {};;
$: prikazi()



</script>



<div class="card">
   
    <div class="container">
      <h4>{name}</h4>
      <p>{opis}</p>
      <button on:mouseenter|once={prikazI}  on:click|once={imeKorisnika(name) }>ime</button>
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