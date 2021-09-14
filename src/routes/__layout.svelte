<script>
  import '../tailwind.css'
  import Header from '../components/Header.svelte'
</script>

<Header />
<div class="w-full min-h-screen bg-gradient-to-r from-yellow-600 via-pink-500 to-purple-500 px-10 md:px-20 lg:px-52 py-20">
  <slot></slot>
</div>
