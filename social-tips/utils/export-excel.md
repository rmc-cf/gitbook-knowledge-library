# 导出Excel

{% code lineNumbers="true" %}
```html
// Vue3实现 xlsx
<script src="https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.18.5/xlsx.full.min.js"></script>
 <script>
 exportToExcel() {
         // 1️⃣ 创建工作簿（Workbook）
         const wb = XLSX.utils.book_new();
         // 2️⃣ 将 JSON 数据转换为工作表（Worksheet）
         const ws = XLSX.utils.json_to_sheet(this.tableData);
         // 3️⃣ 将工作表添加到工作簿
         XLSX.utils.book_append_sheet(wb, ws, "员工信息");
         // 4️⃣ 触发下载
         XLSX.writeFile(wb, "员工信息.xlsx");
  }
   </script>
```
{% endcode %}
