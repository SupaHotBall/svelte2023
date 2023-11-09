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
      "https://www.youtube.com/embed/SQc2jhbGT2k?si=1DGQq0olblMVibZ3",
      "https://www.youtube.com/embed/fueqERLu-Fk?si=Apns2jVo_RotE1GL&start=4",
      "https://www.youtube.com/embed/ia6sRyT6ArE?si=fWr3a2GfZIYFC6nb&start=4",
      "https://www.youtube.com/embed/pzIbP2AUXy8?si=SyqzzAsuVhhSISg2&start=4",
    ];

    if (index >= 0 && index < videoUrls.length) {
      return videoUrls[index];
    } else {
      return ""; // Return an empty URL for invalid indices
    }
  }
</script>

<div class="Gojo-page-background">
  <div class="Name">
    <p class="bounceTxt">ゴチョサトル</p>
    <span>G</span>
    <span>O</span>
    <span>J</span>
    <span>O</span>
    <br />
    <span>S</span>
    <span>A</span>
    <span>T</span>
    <span>O</span>
    <span>R</span>
    <span>U</span>
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
              height="450"
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
