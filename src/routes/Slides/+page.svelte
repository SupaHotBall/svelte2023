<script>
    import { onMount } from 'svelte';
  
    let counter = 1;
  
    // Function executed on component mount
    onMount(() => {
      const intervalId = setInterval(() => {
        const radio = document.getElementById('radio' + counter);
        // Check if the radio button exists
        if (radio) {
          radio.checked = true;
          counter++;
          // Reset counter to 1 if it exceeds 5
          if (counter > 5) {
            counter = 1; 
          }
        } else {
          // Stop the interval if no more radios are found
          clearInterval(intervalId); 
        }
      }, 5000);
  
      // Cleanup the interval when the component is unmounted
      return () => clearInterval(intervalId);
    });
  </script>


<div class="Black-ground">
    <div class="slider">
        <div class="slides">
            <input type="radio" name="radio-btn" id="radio1" />
            <input type="radio" name="radio-btn" id="radio2" />
            <input type="radio" name="radio-btn" id="radio3" />
            <input type="radio" name="radio-btn" id="radio4" />
            <input type="radio" name="radio-btn" id="radio5" />

            <div class="slide first">
                <img src="../image/first-slide.jpeg" alt="" />
            </div>

            <div class="slide">
                <img src="../image/Second-Silder.jpeg" alt="" />
            </div>

            <div class="slide">
                <img src="../image/Third-Silder.png" alt="" />
            </div>

            <div class="slide">
                <img src="../image/Fouth-Silder.jpeg" alt="" />
            </div>

            <div class="slide">
                <img src="../image/Last-Silder.jpg" alt="" />
            </div>

            <div class="navigation-auto">
                <div class="auto-btn1" />
                <div class="auto-btn2" />
                <div class="auto-btn3" />
                <div class="auto-btn4" />
                <div class="auto-btn5" />
            </div>
        </div>

        <div class="navigation-manual">
            <label for="radio1" class="manual-btn" />
            <label for="radio2" class="manual-btn" />
            <label for="radio3" class="manual-btn" />
            <label for="radio4" class="manual-btn" />
            <label for="radio5" class="manual-btn" />
        </div>
    </div>
</div>
