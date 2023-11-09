<script>
  let videoIndex = 0;

  function scrollRight() {
    videoIndex++;
    if (videoIndex >= 2) { // Adjust this based on the number of videos
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
      "https://www.youtube.com/embed/SWRUnpHU7yw?si=iDvFC-NWi_sP7IHr",
      "https://www.youtube.com/embed/MohkTXPEsc8?si=TNERoCYUgteP-3NC",
      "https://www.youtube.com/embed/R1cfvvj1vr0?si=c3PoFV6BvyiNkxfW",
      "https://www.youtube.com/embed/uCkrWgvovY8?si=9cEwjnxDxnitdFKQ"
    ];

    if (index >= 0 && index < videoUrls.length) {
      return videoUrls[index];
    } else {
      return ""; // Return an empty URL for invalid indices
    }
  }
</script>



<div class="Ryomen-page-background">
  <div class="Name">
    <p class="ryomenAnimationText">レオメンスクーナ</p>
    <span>R</span>
    <span>Y</span>
    <span>O</span>
    <span>M</span>
    <span>E</span>
    <span>N</span>
    <br>
    <span>S</span>
    <span>U</span>
    <span>K</span>
    <span>U</span>
    <span>N</span>
    <span>A</span>
  </div>

  <div class="Video-container">
    
    <i class="fa-solid fa-circle-arrow-left fa-2xl left-button" on:click={scrollLeft}></i>

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
          ></iframe>
        </div>
      {/if}
    {/each}
  </div>

    <i class="fa-solid fa-circle-arrow-right fa-2xl right-button" on:click={scrollRight}></i>
</div>
</div>
