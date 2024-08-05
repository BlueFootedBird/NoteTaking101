# Note Taking 101 (Why?)
Penetration Testing and Red Teaming is tough. One of the many challenges of these fields is the infinite amount of information - it's quite literally impossible to contain all of the information at any given time. And if you're like me, I can't remember anybody's birthday, much less the subtle syntax difference between any of Impacket's billion commands.  

In short, if I don't write it down, I likely wont remember it. Therefore, I've spent dozens of hours crafting my notes - combining my intense desire for aesthetic pretty colors with the need for a structured archive of knowledge I've built up over the years. I believe that I've gotten to a point to where my note taking processes might not only help me, but others as well. So, let's dive in.
 
## Note Taking 101
I use Obsidian for my notes, and I believe you should too. If you need a reason for why Obsidian is one of, if not the best note taking apps for penetration testing and red teaming, I'm sorry to tell you that GitHub only allows files up to 25MB, and the answer to the aforementied question takes at least 25GB for me to explain why it's the best. If that sarcastic answer was vague and didn't answer your question at all, keep reading and you'll see why I'm so fond of it. I'll have plenty of examples.

### My Big Three
There are three key tools that I think can transcend your note taking to the next level. Let's talk about each one by one, starting with Flameshot. 

#### Flameshot (The best screenshot tool)
If you're like me, I used to use the classic Windows Snipping tool for years until a coworker of mine introduced me to Flameshot. But, why should you care? What makes it so good? Put simply - It allows you to adjust the bounds of you screenshot while you annotate it. If I wanted to circle or highlight something in a screenshot before - I would use the Snipping tool, paste the image into PowerPoint, and draw on top of the image with arrows and boxes. With Flameshot, I can do that all without PowerPoint in the first place. If you haven't, download Flameshot and give it whirl. See what you can do by using this tool to take more professional screenshots by annotating the important information you want to convey.  
![FlameshotGif](/media/Flameshot.gif)




#### HTML Code Blocks 
When I was preparing for the OSCP, I was faced with a dilemma. The reporting guide demanded that you color/highlight each command that you ran. This is easy if you're using a rich-text editor, but very hard if you want to do it in Markdown. Thus, I spent countless hours fighting with custom CSS to simulate the style of a code block that also lets you color and highlight the text within it.

For example, here's what my notes used to look like (Version 1.0). You can read more about it in this picture.
![Version1](/media/version1.png)

Now, here's what my notes looked like for a while after (Version 1.5)
![Version1.5](/media/version1point5.png)

Now, here's what my notes look like now (Version 2.0)
![Version1.5](/media/version2.gif)


While it might seem trivial, highlighting the commands that you've run makes it easier to reproduce your steps and for somebody reading your notes to understand what you've done. Screenshots can be great, but you can't copy and paste commands from a picture. You can, however, copy and paste directly from this simulated code block. If you're interested in using my CSS settings for Obsidian, I've taken the liberty and attached the `custom.css` file to this repository.

I find that if I'm doing an actual report for a real client - screenshots may be preferred. However, if I'm taking notes or doing a walkthrough for a vulnerable machine, I prefer using these custom HTML code blocks. (Note: I also have an Autoescape feature for my notes where it'll replace any characters that are funky, like `<dir>` - I may add more information about this if people seem interested)

 
#### Templater for Automation
Templater is really quite magical. I use it in my notes for automating report writing, command syntax, and my enumeration methodology. For instance, this is an example of a template I made for not needing to remember the syntax of a tool called bloodhound-python. 
[Screenshot of Templater]

Look at the video below of what happens when I execute this template. When I call this template, it will prompt me for a username, password, dcip, and domain. Once I give it that information, it will construct the command for me and insert it into my notes for me to copy/paste. This might seem like a small improvement, but it helps a lot when I'm under a time crunch and don't want to spend 1-3 minutes trying to remember the syntax of common commands I run. 
[Short Clip of executing the template]

Now onto the part that made me feel confident in publishing something public about my notes. I found myself often missing certain steps of my methodology when I was rushing too fast, or simply just forgot to check for a privilege escalation vector. I was also inspired about the talk found here: 
https://www.youtube.com/watch?v=ydqtyfxY0EA.

Thus, I've scripted out SA commands, Priv Esc commands, and Post-Exploitation commands within Obsidian using Templater. How does that work? Great question. I'll give a brief example of how the SA works..
(Show clip of running SA)

I've also done this for Windows Priv Esc
(Show Clip of running Priv Esc)

Show for Post-Exploitation
(Show clip of Post esclpoktiation)

  

*Youtube video doing a side-by side walkthrough on notes
