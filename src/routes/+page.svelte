<script>

  // Function to close the video
  function closeVideo() {
    const background = document.querySelector('.blur');
    background.classList.remove("blur");
    // showVideo = false;
    const videoContainer = document.querySelector('#container');
    videoContainer.classList.add("hidden");
  }


</script>

<div class="HomePagebase-background blur">
  <div class="body-image" />
</div>

<div id="container">
    <div id="player">
      <iframe
        width="1000"
        height="700"
        src="https://www.youtube.com/embed/PKHQuQF1S8k?si=81o3OE1QGKAMGXB7"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        allowfullscreen
      />
    </div>
    <div class="close-button glow-on-hover" on:click={closeVideo}>Close</div>
  </div>
