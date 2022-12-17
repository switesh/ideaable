<svelte:head>
	<title>{title}</title>
</svelte:head>

<script>
import { goto } from '$app/navigation';
let title = 'Sign up'
</script>

<section class="p-8 lg:p-16">
  <p class="p-8 text-4xl font-bold text-violet-500 text-center"><a href="/" class="btn">ideaable</a></p>
  <form class="p-8 space-y-8 max-w-sm mx-auto">
    <h1>Sign up</h1>
    <div class="input-wrapper">
      <label for="abc">Email</label>
      <input type="text" name="abc">
    </div>
    <div class="input-wrapper">
      <label for="pwd">Password</label>
      <input type="password" name="pwd">
    </div>
    <a href="home" class="btn base primary block text-center">Sign up</a>
  </form>
</section>