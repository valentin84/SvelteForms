<script>
    import Button from './Button.svelte';
    import Popup from './Popup.svelte';
    let modal;

    function isValid() {
    let iban = document.querySelector("#iban").value;
    let ibanError = document.querySelector("#iban");
    let amount = document.querySelector("#amount").value;
    let amountError = document.querySelector("#amount");
    if(iban === '' || amount == '') {
        return false
        
    } else {
        return true;
         
    }
}

</script>


<label for="iabn">IBAN</label>
<input type="text" minlength="13" id="iban" required>

<label for="amount">Amount</label>
<input maxlength={9} id="amount" required>

<Button on:click={() => { isValid() == true ? modal.open() : ""}} name={"Send"} />

<Popup bind:this={modal} />



<style>
 
</style>