<script>
  import back from '../../../static/backIcon.svg';
  import home from '../../../static/homeIcon.svg';
  import {goto} from '$app/navigation';

  const goBack = () => {
    window.history.back()
  }
</script>

<div class="flex items-center justify-between mb-12">
  <button on:click={goBack} class="flex items-center justify-center text-white">
    <img src={back} alt="back" class="h-4">
    <div class="ml-2">Back</div>
  </button>
  <button on:click={() => {goto('/')}} class="flex items-center justify-center text-white">
    <img src={home} alt="back" class="h-5">
  </button>
</div>
<slot></slot>
