**Urgent Stuff:**
```dataview
LIST from #urgent 
```
Overdue:
```tasks
not done
sort by due date
due before <% tp.date.now("YYYY-MM-DD")%>
hide backlinkg
```
___
Due Today:
```tasks
not done 
due <% tp.date.now("YYYY-MM-DD") %>
sort by priority
```
___
Unscheduled
```tasks
not done
no due date
```
___
