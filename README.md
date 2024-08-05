# Note Taking 101 (Why?)
Penetration Testing and Red Teaming is tough. One of the many challenges of these fields is the infinite amount of information - it's quite literally impossible to contain all of the information at any given time. And if you're like me, I can't remember anybody's birthday, much less the subtle syntax difference between any of Impacket's billion commands.  

In short, if I don't write it down, I likely wont remember it. Therefore, I've spent dozens of hours crafting my notes - combining my intense desire for aesthetic pretty colors with the need for a structured archive of knowledge I've built up over the years. I believe that I've gotten to a point to where my note taking processes might not only help me, but others as well. So, let's dive in.
 
# Note Taking 101 (How?)
I use Obsidian for my notes, and I believe you should too. If you need a reason for why Obsidian is one of, if not the best note taking apps for penetration testing and red teaming, I'm sorry to tell you that GitHub only allows files up to 25MB, and the answer to the aforementied question takes at least 25GB for me to explain why it's the best. If that sarcastic answer was vague and didn't answer your question at all, keep reading and you'll see why I'm so fond of it. I'll have plenty of examples.

## My Big Three
There are three key tools that I think can transcend your note taking to the next level. Let's talk about each one by one, starting with Flameshot. 

### 1. Flameshot (The best screenshot tool)
If you're like me, I used to use the classic Windows Snipping tool for years until a coworker of mine introduced me to Flameshot. But, why should you care? What makes it so good? Put simply - It allows you to adjust the bounds of you screenshot while you annotate it. If I wanted to circle or highlight something in a screenshot before - I would use the Snipping tool, paste the image into PowerPoint, and draw on top of the image with arrows and boxes. With Flameshot, I can do that all without PowerPoint in the first place. If you haven't, download Flameshot and give it whirl. See what you can do by using this tool to take more professional screenshots by annotating the important information you want to convey.  
![FlameshotGif](/media/Flameshot.gif)




### 2. HTML Code Blocks 
When I was preparing for the OSCP, I was faced with a dilemma. The reporting guide demanded that you color/highlight each command that you ran. This is easy if you're using a rich-text editor, but very hard if you want to do it in Markdown. Thus, I spent countless hours fighting with custom CSS to simulate the style of a code block that also lets you color and highlight the text within it.

For example, here's what my notes used to look like (Version 1.0). When I first started trying to highlight the commands I ran, I hit a problem where the boxes I'd use looked rather clunky. Also, depending on how much text I had on the screen, the size of the font in the screenshot would vary, creating some inconsitency between screenshots. Sometimes the border of the box would cut off some characters, and while this worked for a while, I felt that I could do better.
![Version1](/media/version1.png)

Introducting Version 1.5 of my notes. It still relied on using Flameshot, but I swapped from using the box-feature in Flameshot to the highlighter. This looked a little bit nicer and was less abrasive to the eyes. However, sometimes I'd need to highlight over each line a couple of times to get the darkness of the color that I wanted, which became time-consuming. This iteration of my notes still didn't fix the issue that I can't copy/paste text from the screenshots.
![Version1.5](/media/version1point5.png)

Here's the current iteration of my notes - Version 2.0. You might need to manually play the Gif if it doesn't autostart. Version 2.0 involves using HTML in markdown to render my terminal output like a codeblock while still allowing me to highlight and colorize whatever text I want inside `<span>` tags. Now I can copy/paste the output from my notes, and they look glorious. Another point to mention is that pictures take up a much larger amount of space on your drive than raw text, so this saves a lot of space down the road by removing the need to fill my notes with pictures.
![Version1.5](/media/version2.gif)


While it might seem trivial, highlighting the commands that you've run makes it much easier for you to reproduce your steps AND for somebody reading your notes to understand what you've done. Screenshots can be great, but you can't copy and paste commands from a picture. You can, however, copy and paste directly from this simulated code block. If you're interested in using my CSS settings for Obsidian, I've taken the liberty and attached the `custom.css` file to this repository. With the .css file, anything wrapped in a `<pre>` tag will be shown as a code block. I combine this with the community plugin "Colored Text" and "Wrap with shortcuts" to automatically color text with a shortcut.  

I find that if I'm doing an actual report for a real client - screenshots may be preferred. However, if I'm taking notes or doing a walkthrough for a vulnerable machine, I greatly prefer using these custom HTML code blocks. (Note: I also have an Autoescape feature for my notes where it'll replace any characters that are funky, like `<dir>` - I may add more information about this if people seem interested)

 
### 3. Templater for Automation

#### 3.a I don't remember syntax 

Templater is really quite magical. I use it in my notes for automated report writing, command syntax, and my enumeration methodology. For instance, this is an example of a template I made for when I forget the syntax of a tool called bloodhound-python. 
![BloodHoundPython](/media/bloodhoundpython.png)

Look at the video below of what happens when I execute this template. When I call this template, it will prompt me for a username, password, dcip, and domain. Once I give it that information, it will construct the command for me and insert it into my notes for me to copy/paste. This might seem like a small improvement, but it helps a lot when I'm under a time crunch and don't want to spend 1-3 minutes trying to remember the syntax of common commands I run. This can be executed from anywhere in Obsidian, not just when I'm on this note.
![Templater1](/media/templater1.gif)

#### 3.b I don't remember my methodology

Now onto the part that made me feel confident in publishing something about my notes. I found myself often missing certain steps of my methodology when I was rushing too fast, or simply just forgot to check for a privilege escalation vector. I was also inspired about the talk found here that empahsizes the importance of checklists: https://www.youtube.com/watch?v=ydqtyfxY0EA. 

Thus, I've scripted out SA commands, Priv Esc commands, and Post-Exploitation commands within Obsidian using Templater. How does that work? Great question. I'll give a brief example of how the SA works. When I run the template called "(SA) Windows" Templater automatically creates a subfolder called "SituationalAwareness" in the current directory of the note I ran the template from. The template also creates subnotes in that folder pre-populated with content for me to copy/paste, as well as connecting/linking the subnotes to the note I wanted to run the SA commands on. This allows me to easily navigate back and forth between the SA notes and my walkthrough of the machine to make sure I'm hitting each checklist.
![Templater1](/media/templater2.gif)


I've also done this for Windows Privilege Escalation, which takes the groundwork I laid for the "(SA) Windows" Template script and pumps it full of steriods. 
![Templater1](/media/templater3.gif)

(TODO - A work in progress)