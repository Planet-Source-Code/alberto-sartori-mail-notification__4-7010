<div align="center">

## Mail notification


</div>

### Description

This code send a message to a specified address as a notification of the main mail message. Usually tells you if the message has been read or deleted.
 
### More Info
 
It return a mail message of notification.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Alberto Sartori](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/alberto-sartori.md)
**Level**          |Beginner
**User Rating**    |4.5 (18 globes from 4 users)
**Compatibility**  |ASP \(Active Server Pages\)
**Category**       |[Algorithims](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/algorithims__4-29.md)
**World**          |[ASP / VbScript](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/asp-vbscript.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/alberto-sartori-mail-notification__4-7010/archive/master.zip)





### Source Code

```
<%
' MAIL NOTIFICATION, by RaS! (ras78@libero.it) 2001
' This simple example send a mail to the main address and a
' notify message to another one. You will receive a message that
' tell you if the main message has been read or deleted.
Set MyMail = Server.CreateObject("CDONTS.NewMail")
 MyMail.From = "sender@domain.com"
 MyMail.To = "second_address@domain.com"
 MyMail.Subject = "Hello World!"
 MyMail.Body = "Email test with notify"
 MyMail.Value("Disposition-Notification-To")="other_address@domain.com"
 MyMail.Send
Set MyMail = Nothing
%>
```

