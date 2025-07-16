ToDoItem.vue 需求規格說明

Props 定義：
Label：必填屬性，型別為 String。用來顯示在待辦項目旁的標籤（label）。
done：可選屬性，型別為 Boolean，預設值可為 false，代表該待辦項目是否已完成。

Component Data：
isDone：用來追蹤該待辦項目的完成狀態，與 done prop 進行同步或雙向綁定。
ID：每個待辦項目的唯一識別碼，格式為 "todo-" 前綴加上 UUID（全域唯一識別碼）。此 ID 用於 input 元素的 id 屬性。

Template 組成：
外層容器：使用 <div> 元素包裹整個待辦項目。

Input 元素：
類型為 checkbox，代表是否完成。
id 屬性需與 Label 相關聯，ID 格式為 "todo-" + UUID。
需與 isDone 進行雙向綁定（即當用戶點擊 checkbox 時，isDone 的值會相應改變，反之亦然）。

Label 元素：
文字內容由 Label prop 提供。
for 屬性設為與 input 相同的 ID，以建立關聯。

雙向綁定與同步：
input checkbox 的狀態與 isDone 變數雙向綁定。
當 done prop 改變時，isDone 也應同步更新（或使用適當的方式保持同步）。
Label 文字應由 prop 提供，且可動態更新（如果有需要的話）。

其他：
請確保每個待辦項目的 ID 是獨一無二的，且格式統一。
相關屬性與事件應符合 Vue 的標準做法，方便維護與擴充。