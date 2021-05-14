<script>
    import Button from './Button.svelte';
    let isOpen = false;

    export function open() {
        isOpen = true;
    }
    function validate() {
        let token = document.querySelector("#token").value;
        if(token === '') {
            return false
        
        } else {
            return true;          
        }
    }
    function close() {
        isOpen = false;      
    }
    
    
</script>



{#if isOpen}
<div class="modal">
    <div class="popup">
        <form action="">   
            <label for="token">Token</label>
            <input minlength={8} id="token" required >
            <Button on:click={() => {validate() == true ? close() : ''}} name={"Close"} />
        </form>     
    </div>
</div>   
{/if} 



<style>
    .modal {
        position: absolute;
        width: 100%;
        height: 100%;
        background-color: #000;
        opacity: 0.4;
        z-index: 1;
        top: 0;
        left: 0;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .popup {
        margin: 0 auto;
        max-width: 300px;
        width: 20%;
        background-color: yellow;
        padding: 20px;
    }
</style>