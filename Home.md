
```dataview
LIST from #urgent and !"templates"
```
Todo:
```tasks
not done
sort by priority
happens this week
```
___
Overdue:
```tasks
not done
sort by due date
due before <% tp.date.now("YYYY-MM-DD")%>
hide backlink
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
Overall:
```tasks
not done
```
