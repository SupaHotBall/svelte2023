<script>
  let videoIndex = 0;

  function scrollRight() {
    videoIndex++;
    if (videoIndex >= 2) {
      // Adjust this based on the number of videos
      videoIndex = 2;
    }
  }

  function scrollLeft() {
    videoIndex--;
    if (videoIndex < 0) {
      videoIndex = 0;
    }
  }

  function getVideoUrl(index) {
    const videoUrls = [
      "https://www.youtube.com/embed/sy1Kdw1V0r0?si=r1rXZ0-II6G9EOvU",
      "https://www.youtube.com/embed/UeOTYQwlUtA?si=ckft7GhTAi5IqG7v",
      "https://www.youtube.com/embed/2V_O7lH3NRQ?si=8wTra3DCm97Il_YG",
      "https://www.youtube.com/embed/SCAiB_AKu9U?si=e81cuSkyOAEdNOKB",
    ];

    if (index >= 0 && index < videoUrls.length) {
      return videoUrls[index];
    } else {
      return ""; // Return an empty URL for invalid indices
    }
  }
</script>

<div class="Kento-page-background">
  <div class="Name">
    <div class="kentoAnimationText" />
    <span>K</span>
    <span>E</span>
    <span>N</span>
    <span>T</span>
    <span>O</span>
    <br />
    <span>N</span>
    <span>A</span>
    <span>N</span>
    <span>A</span>
    <span>M</span>
    <span>I</span>
  </div>

  <div class="Video-container">
    <i
      class="fa-solid fa-circle-arrow-left fa-2xl left-button"
      on:click={scrollLeft}
    />

    <div class="video-scroll-container">
      {#each [1, 2, 3, 4] as video, i}
        {#if i >= videoIndex && i < videoIndex + 3}
          <div class="video-wrapper">
            <iframe
              width="560"
              height="315"
              src={getVideoUrl(i)}
              title="YouTube video player"
              frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
              allowfullscreen
            />
          </div>
        {/if}
      {/each}
    </div>

    <i
      class="fa-solid fa-circle-arrow-right fa-2xl right-button"
      on:click={scrollRight}
    />
  </div>
</div>
