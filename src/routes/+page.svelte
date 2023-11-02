<script>
  import { onMount } from 'svelte';

  let player;
  let showVideo = false;

  onMount(() => {
    // Load the YouTube iframe API when the component is mounted
    const script = document.createElement('script');
    script.src = 'https://www.youtube.com/iframe_api';
    document.body.appendChild(script);

    script.onload = () => {
      window.onYouTubeIframeAPIReady = () => {
        player = new YT.Player('player', {
          height: '315', // Adjust to your desired height
          width: '560',  // Adjust to your desired width
          videoId: 'PKHQuQF1S8k', // Replace with your video ID
          events: {
            'onReady': onPlayerReady,
          },
        });
      };
    };
  });

  // Function to start playing the video when it's ready
  function onPlayerReady(event) {
    event.target.playVideo();
    showVideo = true;
  }

  // Function to close the video
  function closeVideo() {
    player.stopVideo();
    showVideo = false;
  }

  // Event listener to close the video when the "Escape" key is pressed
  window.addEventListener('keydown', (event) => {
    if (event.key === 'Escape' && showVideo) {
      closeVideo();
    }
  });
</script>

<div class="HomePagebase-background">
  <div class="body-image"></div>
</div>

<div id="container">
  <div id="player"></div>
  {#if showVideo}
    <div class="close-button" on:click={closeVideo}>Close</div>
  {/if}
</div>
