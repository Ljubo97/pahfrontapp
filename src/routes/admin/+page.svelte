<script>
    
    import Korisnik from "./korisnik.svelte";
    let naziv = "Admin"
    let naslov = "Dobrodosli na Admin Stranicu"
    const kor={
name: "djordje", opis:"Sto ima props" 
    }
  const target={
    ...kor
  }
    $:console.log(naziv);

    let value 
    async function onInput(){
        const input = this;
         
        value = input.value.toUpperCase()
       

input.value=value
    }
    function prikazi(){
      console.log(200)
    }
  

    /**
     * @param {any} KorisnikName
     */
    function imeKorisnika(KorisnikName) {
    console.log("Korisnik: " , KorisnikName)

 }
</script>


<Korisnik {imeKorisnika} name="Korisnik 1" opis="Ogranicene dozvole pristupa" {prikazi}/>
<Korisnik {imeKorisnika} name="Korisnik 2" opis="Ogranicene dozvole pristupa" />
<Korisnik {imeKorisnika}  {...kor} />

<Korisnik name={naziv} opis={naslov} {imeKorisnika}/>
