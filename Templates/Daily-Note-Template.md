---
Date: <% tp.date.now() %>
Author: Jimmy Briggs <jimmy.briggs@jimbrig.com>
Alias: []
---
Tags:: [[+Daily Notes]]

<< [[<% tp.date.now("YYYY-MM-DD-dddd", -1, tp.file.title, "YYYY-MM-DD-dddd") %>]] | [[<% tp.date.now("YYYY-MM-DD-dddd", 1, tp.file.title, "YYYY-MM-DD-dddd") %>]]>>

# <% moment(tp.file.title,'YYYY-MM-DD').format("dddd, MMMM DD, YYYY") %>

---
## Day Planner

- [ ] 08:00 Wakeup and Startup
- [ ] 12:00 Lunch
- [ ] 17:00 Shutdown

---
## Agendas
-

---
## Notes
-

---
### Notes Created Today:

```dataview
List FROM "" WHERE file.cday = date("<%tp.date.now("YYYY-MM-DD")%>") SORT file.ctime asc
```

---
### Notes Modified Today:

```dataview
List FROM "" WHERE file.mday = date("<%tp.date.now("YYYY-MM-DD")%>") SORT file.mtime asc
```

***

## Appendix: Links and References

- [[Templates/Daily-Notes/_README|Daily Notes]]

***

Jimmy Briggs <jimmy.briggs@jimbrig.com> | <% tp.date.now("YYYY") %>
