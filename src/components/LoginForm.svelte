<script>
  let text = "";
  let password = "";

  function login() {
    switch (password) {
      case "錯誤的":
        text = "請再試一次";
        break;
      case "一次":
        text = "bruh";
        break;
      default:
        text = "密碼是錯誤的";
        break;
    }
  }
</script>

<div class="flex flex-col gap-5 rounded-xl bg-neutral-800 p-10">
  <h2
    class="text-center text-4xl font-thin text-neutral-200 transition-[color] hover:text-white"
  >
    登入
  </h2>
  <div class="flex flex-col gap-1">
    <input
      type="text"
      placeholder="用戶名稱"
      value="新手Newhand"
      readonly
      class="c-input-text"
    />
    <input
      type="text"
      placeholder="密碼"
      bind:value={password}
      class="c-input-text"
    />
  </div>
  <button on:click={login} class="c-input-button">登入</button>
  <div class="text-center text-red-300">{text}</div>
</div>
