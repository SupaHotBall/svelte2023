<script>
  import { onMount } from 'svelte';
  let player;

  onMount(() => {
    // Load the YouTube iframe API and create the player when the component is mounted
    const script = document.createElement('script');
    script.src = 'https://www.youtube.com/iframe_api';
    document.body.appendChild(script);

    script.onload = () => {
      window.onYouTubeIframeAPIReady = () => {
        player = new YT.Player('player', {
          height: '90%',
          width: '90%',
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
  }
</script>

<div class="HomePagebase-background">
  <div class="body-image"></div>
</div>

<div id="videoContainer">
  <div id="player"></div>
</div>

