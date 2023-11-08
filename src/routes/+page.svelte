<script>
  // Function to close the video
  function closeVideo() {
    const background = document.querySelector(".blur");
    background.classList.remove("blur");
    // showVideo = false;
    const videoContainer = document.querySelector("#container");
    videoContainer.classList.add("hidden");
  }
</script>

<div class="HomePagebase-background blur">
  <div class="body-image" />
</div>

<div id="container">
  <div id="player">
    <iframe
      width="560"
      height="315"
      src="https://www.youtube-nocookie.com/embed/PKHQuQF1S8k?&autoplay=1&rel-0"
      title="YouTube video player"
      frameborder="0"
      allow="autoplay; encrypted-media;"
      allowfullscreen
    />
  </div>
  <div class="close-button glow-on-hover" on:click={closeVideo}>Close</div>
  
</div>
