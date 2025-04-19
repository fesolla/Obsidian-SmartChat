
Smart Chat無法使用Enter直接送出訊息，因此我對程式碼進行了修改。
為避免插件更新後被覆蓋，特別記錄下來。
將\Vault\.obsidian\plugins\smart-connections當中的main.js檔案以下段落
```
  console.log("chat_input", chat_input);
    if (chat_input) {
    chat_input.addEventListener("keydown", async (e) => {
      const is_mod = this.adapter.is_mod_event(e);
      if (e.key === "Enter" && (is_mod || e.ctrlKey || e.metaKey)) {
        e.preventDefault();
        await send_message(chat_input, thread);
        return;
      }
    });
    chat_input.addEventListener("keyup", (e) => handle_chat_input_keyup.call(this, e, chat_input));
  }
```

更改為
```
if (chat_input) {
  chat_input.addEventListener("keydown", async (e) => {
    if (e.key === "Enter" && !e.shiftKey) {
      e.preventDefault();
      await send_message(chat_input, thread); 
      return;
    }
  });

  chat_input.addEventListener("keyup", (e) => handle_chat_input_keyup.call(this, e, chat_input));
}
```