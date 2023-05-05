If you have a large dataset with empty rows, you may need to remove them to avoid skewing your analysis. Design a workflow to remove the empty rows in the given Excel sheet. 

Dependencies/packages- UiPath.Excel.Activties

Activities required
-Read range
-Assign Activity {value to save syntax = varname.AsEnumerable().Where(Function(row) Not row.ItemArray.All(Function(field) field Is Nothing OrElse field Is DBNull.Value OrElse field.Equals("") OrElse field.Equals(" "))).CopyToDataTable() }
-write range