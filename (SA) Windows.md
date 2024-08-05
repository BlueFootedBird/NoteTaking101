# Windows Priv Esc Checks
<%* 
path = "/" + tp.file.folder(true) + "/SituationalAwareness/"

fileName = "User and Group Permissions"
await tp.file.create_new(tp.file.find_tfile("(SA) Windows User and Group Permissions"), "", false)
await tp.file.move(path + fileName)

fileName = "System Information"
await tp.file.create_new(tp.file.find_tfile("(SA) Windows System Information"), "", false)
await tp.file.move(path + fileName)

fileName = "Networking Enumeration"
await tp.file.create_new(tp.file.find_tfile("(SA) Windows Network Enumeration"), "", false)
await tp.file.move(path + fileName)

fileName = "Installed Software"
await tp.file.create_new(tp.file.find_tfile("(SA) Windows Installed Software"), "", false)
await tp.file.move(path + fileName)

fileName = "Running Processes"
await tp.file.create_new(tp.file.find_tfile("(SA) Windows Running Processes"), "", false)
await tp.file.move(path + fileName)

%>

---
<p class="center-italic">Situational Awareness
</p>
---

- [ ] [[<% tp.file.folder(true) + "/User and Group Permissions"%>|User and Group Permissions]]
- [ ] [[<% tp.file.folder(true) + "/System Information"%>|System Information]]
- [ ] [[<% tp.file.folder(true) + "/Networking Enumeration"%>|Networking Enumeration]]
- [ ] [[<% tp.file.folder(true) + "/Installed Software" %>|Installed Software]] 
- [ ] [[<% tp.file.folder(true) + "/Running Processes" %>|Running Processes]]



