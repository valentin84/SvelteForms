<script>
    export function isValid() {
    let iban = document.querySelector("iban").value;
    let ibanError = document.querySelector("iban");
    if(iban === '') {
        return false;
    } else {
        return true;
    }
}

export function open() {
    isOpen = true;
}

export function close() {
    let input = document.querySelector("#token");
    let token = document.querySelector("#token").value;
    if(token.length !== 8) {
        input.setCustomValidity("Must input 8 alphanumeric characters");
    } else {
        isOpen = false;
    }
    
}
</script>