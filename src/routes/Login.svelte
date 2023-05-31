<script>
	import { userName } from "../routes/store";
</script>

<div class="login">
  <div class="block-info">
    <h1>Welcome to my Portfolio</h1>
    <h3>Please enter your name below to login</h3>
    <h6>Your login name will not be stored anywhere</h6>
  </div>
  <div class="user-input">
    <input type="text" bind:value={$userName} autocomplete="off">
    {#if $userName}
      <p>{$userName}</p>
      <a href="/desktop">click</a>
    {:else}
      <p>Enter a User Name</p>
    {/if}
  </div>
</div>

<style>
  .login {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    flex: 0.6;
  }
  .block-info, .user-input {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
</style>
