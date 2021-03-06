<!-- default file list -->
*Files to look at*:

* [Default.aspx](./CS/WebSite/Default.aspx) (VB: [Default.aspx](./VB/WebSite/Default.aspx))
* [Default.aspx.cs](./CS/WebSite/Default.aspx.cs) (VB: [Default.aspx.vb](./VB/WebSite/Default.aspx.vb))
<!-- default file list end -->
# ASPxGridView - How to add a column if the AutoGenerateColumns property is set to true
<!-- run online -->
**[[Run Online]](https://codecentral.devexpress.com/e3587/)**
<!-- run online end -->


<p>When the  <a href="http://documentation.devexpress.com/#AspNet/DevExpressWebASPxGridViewASPxGridView_AutoGenerateColumnstopic"><u>AutoGenerateColumns</u></a> property is set to true, the only way to add a column to ASPxGridView is to handle the ASPxGridView.DataBound event. To avoid creating duplicate columns, it is necessary to add a condition that will check whether a column already exists. For example:</p>

```cs
protected void ASPxGridView1_DataBound(object sender, EventArgs e) {
    if (grid.Columns.IndexOf(grid.Columns["CommandColumn"]) != -1)
            return;
    GridViewCommandColumn col = new GridViewCommandColumn();
    col.Name = "CommandColumn";
    grid.Columns.Add(col);
}
```

<p> </p><p><strong>See also:</strong><br />
<a href="https://www.devexpress.com/Support/Center/p/E20054">GridView - How to add a column if the AutoGenerateColumns property is set to true</a></p><br />


<br/>


