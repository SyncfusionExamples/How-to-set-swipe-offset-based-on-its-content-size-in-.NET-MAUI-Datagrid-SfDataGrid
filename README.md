# How to set swipe offset based on its content size in .NET MAUI Datagrid (SfDataGrid) ?
In this article, we will show you how to set swipe offset based on its content size in in [.NET MAUI DataGrid](https://www.syncfusion.com/maui-controls/maui-datagrid).

## xaml
The code below demonstrates how to set swipe offset based on its content size in DataGrid.
```
<ContentPage.BindingContext>
    <local:EmployeeViewModel x:Name="viewModel" />
</ContentPage.BindingContext>

<syncfusion:SfDataGrid x:Name="dataGrid"
                       ItemsSource="{Binding Employees}"
                       ColumnWidthMode="Auto"
                       AutoGenerateColumnsMode="None"
                       GridLinesVisibility="Both"
                       SwipeOffsetMode="Auto"
                       HeaderGridLinesVisibility="Both"
                       AllowSwiping="True">
    <syncfusion:SfDataGrid.LeftSwipeTemplate>
        <DataTemplate>
            <Grid BackgroundColor="Blue"
                  Padding="9">
                <Label Text="EDIT"
                       HorizontalTextAlignment="End"
                       TextColor="#FFFFFF"
                       VerticalTextAlignment="Center"
                       LineBreakMode="NoWrap"
                       BackgroundColor="Transparent" />
            </Grid>
        </DataTemplate>
    </syncfusion:SfDataGrid.LeftSwipeTemplate>

    <syncfusion:SfDataGrid.RightSwipeTemplate>
        <DataTemplate>
            <Grid BackgroundColor="Red"
                  Padding="9">
                <Label FontSize="15"
                       HorizontalTextAlignment="Center"
                       Text="Delete"
                       TextColor="White"
                       VerticalTextAlignment="Center"
                       LineBreakMode="NoWrap" />
            </Grid>
        </DataTemplate>
    </syncfusion:SfDataGrid.RightSwipeTemplate>

    <syncfusion:SfDataGrid.Columns>
        <syncfusion:DataGridNumericColumn MappingName="EmployeeID"
                                          Format="#"
                                          HeaderText="Employee ID" />
        <syncfusion:DataGridTextColumn MappingName="Name"
                                       HeaderText="Employee Name" />
        <syncfusion:DataGridTextColumn MappingName="Title"
                                       HeaderText="Designation" />
        <syncfusion:DataGridDateColumn MappingName="HireDate"
                                       HeaderText="Hire Date" />

    </syncfusion:SfDataGrid.Columns>
</syncfusion:SfDataGrid>
``` 
**Note**
The value of the [SfDataGrid.MaxSwipeOffset](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html?tabs=tabid-1#Syncfusion_Maui_DataGrid_SfDataGrid_MaxSwipeOffset) property will not be considered when the [SfDataGrid.SwipeOffsetMode](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html#Syncfusion_Maui_DataGrid_SfDataGrid_SwipeOffsetMode) is set to [SwipeOffsetMode.Auto](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridSwipeOffsetMode.html#Syncfusion_Maui_DataGrid_DataGridSwipeOffsetMode_Auto).

<img src="https://support.syncfusion.com/kb/agent/attachment/inline?token=eyJhbGciOiJodHRwOi8vd3d3LnczLm9yZy8yMDAxLzA0L3htbGRzaWctbW9yZSNobWFjLXNoYTI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjM0OTUwIiwib3JnaWQiOiIzIiwiaXNzIjoic3VwcG9ydC5zeW5jZnVzaW9uLmNvbSJ9.ILKIIxDGhC_ZuuVhxwcXwLc6vX6JCvDGJPL1JfkqR4o" width=700 />

[View sample in GitHub](https://github.com/SyncfusionExamples/How-to-set-swipe-offset-based-on-its-content-size-in-.NET-MAUI-Datagrid-SfDataGrid)

Take a moment to explore this [documentation](https://help.syncfusion.com/maui/datagrid/overview), where you can find more information about Syncfusion .NET MAUI DataGrid (SfDataGrid) with code examples. Please refer to this [link](https://www.syncfusion.com/maui-controls/maui-datagrid) to learn about the essential features of Syncfusion .NET MAUI DataGrid (SfDataGrid).
 
##### Conclusion
 
I hope you enjoyed learning about how to set swipe offset based on its content size in .NET MAUI DataGrid (SfDataGrid).
 
You can refer to our [.NET MAUI DataGrid’s feature tour](https://www.syncfusion.com/maui-controls/maui-datagrid) page to learn about its other groundbreaking feature representations. You can also explore our [.NET MAUI DataGrid Documentation](https://help.syncfusion.com/maui/datagrid/getting-started) to understand how to present and manipulate data. 
For current customers, you can check out our .NET MAUI components on the [License and Downloads](https://www.syncfusion.com/sales/teamlicense) page. If you are new to Syncfusion, you can try our 30-day [free trial](https://www.syncfusion.com/downloads/maui) to explore our .NET MAUI DataGrid and other .NET MAUI components.
 
If you have any queries or require clarifications, please let us know in the comments below. You can also contact us through our [support forums](https://www.syncfusion.com/forums), [Direct-Trac](https://support.syncfusion.com/create) or [feedback portal](https://www.syncfusion.com/feedback/maui?control=sfdatagrid), or the feedback portal. We are always happy to assist you!