<script>
    import authorKeypair from "../store/identity.js";

    import { createEventDispatcher } from 'svelte';

    const dispatch = createEventDispatcher();


    let fileinput;
    let alias;
    let src = 'images/upload-img.png';


    // read identity file as json
    function readFileAsync(file) {
    return new Promise((resolve, reject) => {
      let reader = new FileReader();
      reader.onload = () => {
        resolve(reader.result);
      };
      reader.onerror = reject;
      reader.readAsBinaryString(file);
    });
  }
    // select file and set keypair
    async function onFileSelected(e) {
        // from the file selected
        let fileAttachment = e.target.files[0];
        let fileReady = await readFileAsync(fileAttachment);
        try {
          let keypairObject = JSON.parse(fileReady);
          dispatch('newIdentity', keypairObject); // Dispatch the entire new identity.
        } catch (error) {
            dispatch('error');
        }
    }



</script>

<input
    style="display:none"
    type="file"
    accept=".json, .txt"
    on:change={(e) => onFileSelected(e)}
    bind:this={fileinput}
/>
<div class='flex w-auto lg:w-11/12 items-center align-center flex-col'>
<button 
    class='tooltip phase1 my-2 '
    on:click={() => {fileinput.click()}}>
    
    Upload your current alias in .JSON

    <span class="tooltiptext">It is a JSON file</span>
</button>
</div>
