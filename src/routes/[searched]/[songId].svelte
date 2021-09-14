<script context="module">
  export async function load({page}) {
    var songId = page.params.songId;
    const itunesSearched = await fetch(`https://itunes.apple.com/search?term=${songId}&entity=song`);
    var res = await itunesSearched.json();
    var songResults = res.results[0];
    return {props: {songResults}}
  }
</script>
<script>
  export let songResults;
</script>

<section>
  <div class="mt-12 flex flex-col items-center justify-center">
    <h1 class="text-3xl font-bold text-center mb-12">{songResults.trackName}</h1>
    <img src={songResults.artworkUrl100} alt="img" class="w-1/4 rounded-md mb-12">
    <audio controls>
      <source src={songResults.previewUrl} type="audio/mpeg">
    </audio>
  </div>
</section>
