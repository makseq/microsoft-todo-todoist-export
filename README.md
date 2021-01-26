# Export tasks from microsoft todo to Todoist

It's only a semi-automated export wihtout nested subtasks and subdata. 

1 Open browser console in todo microsoft

2 Open task list you want to export

3 Run this code in console:

```
csv = 'TYPE,CONTENT,PRIORITY,INDENT,AUTHOR,RESPONSIBLE,DATE,DATE_LANG,TIMEZONE\n';
ts = document.getElementsByClassName("taskItem-title");
for (var i=0; i<ts.length; i++) {
  csv += 'task,"' + ts[i].textContent + '",4,1,Max (32188958),,,en,Europe/Moscow' + '\n';
```

4 Reformat (if need) output csv to your awesome todo software.

