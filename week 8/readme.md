
# WEEK 8

# Research a new language

## Language: Lua

## What is Lua used for?
Lua is a small, lightweight scripting language mainly used for game development and embedded systems. It is implemented in C or C++ and designed to be easily embedded into applications. Lua has been used in major games such as World of Warcraft and Angry Birds, where it handles in-game scripting and logic. It is also used in software applications like Adobe Photoshop Lightroom for customization and automation. Because of its small size and high performance, Lua is especially popular in environments where efficiency and portability are important.

## Who uses Lua?
Lua is used by game developers, software companies, security tool developers, and embedded systems engineers. Game studios such as Blizzard Entertainment use Lua in games like World of Warcraft to power UI customization and addons/mods. Major software companies like Adobe Inc. embed Lua in applications such as Adobe Photoshop Lightroom for scripting and automation. Security and networking professionals use tools like Wireshark, which include Lua scripting engines for additional functionality. Embedded systems developers use Lua in environments where performance and small memory are important.

## What are some useful resources?
There are many useful resources for learning Lua, the best one would be the official reference manual on Lua.org, which provides a clear view of the language syntax and features. 
https://www.lua.org/manual/5.5/


The Lua mailing list is another valuable resource, because it allows learners to ask questions and engage directly with the active developer community.
https://www.lua.org/lua-l.html


Stack Overflow
Community Q&A site with many Lua questions and answers. Useful for quickly finding solutions to common issues and learning from other developers experiences.
https://stackoverflow.com/questions/tagged/lua

## Why are these specific resources useful?
Lua Reference Manual – Provides documentation straight from the Lua team, ensuring you are learning correct syntax and language features. It’s the foundation for understanding how Lua works.

Lua Mailing List – Connects you to the active Lua community, allowing you to ask questions, ask problems, and get advice from experienced developers. Real-world guidance like this helps you apply Lua and understand it better in projects.

Stack Overflow – Offers practical problem-solving through community Q&A. You can quickly find solutions to common issues, see multiple approaches, and learn from examples shared by other developers and users.

## Examples
 X = 1       -- Ok, global by default
     do
       global Y  -- voids the implicit initial declaration
       Y = 1     -- Ok, Y declared as global
       X = 1     -- ERROR, X not declared
     end
     X = 2       -- Ok, global by default again

     In Lua, variables are global by default, so X = 1 automatically creates a global variable. Inside a do … end block, using global Y disables the default behavior, meaning only explicitly declared globals or locals are allowed—hence X = 1 inside the block causes an error. After the block, Lua returns to global-by-default, so X = 2 works again. This differs from languages like Python, where variables are local by default and globals must be explicitly declared. I have not personally used or learned C or C++, but some of this code does look a bit similar.


## Summary
Overall, I think Lua is a pretty interesting language, it seems like it's a bit complex and more "math" like then some other languages. It is also written in C or C++, and I have not learned anything about those languages, but from skimming through the examples I can sort of get an idea of what to do.



# Write A User Story

App: Instagram
Feature: Posting a Photo

User Story:

"As a user, I want to post a photo so my friends can see."


Specific User Story:

From Camera Roll
"As a user, I want to pick a photo from my phone so I can share a pic I already took."

Taking a New Photo
"As a user, I want to take a new photo in the app so I can post it right away."

Editing Before Posting
"As a user, I want to add filters or change exposure so my photo looks cooler before I post it."

Adding a Caption
"As a user, I want to write a caption so people know what the photo is about."

Tagging Friends
"As a user, I want to tag my friends so they are apart of it, and get notified when its posted."

Adding Location
"As a user, I want to add a location so people know where I took the photo."

Choosing Who Sees It
"As a user, I want to choose who can see my photo and who cant see it to keep my privacy."

Acceptance Criteria:

I can pick photos from my phone.

I can add filters and adjust stuff like brightness and exposure.

I can write a caption.

I can tag friends in the photo.

I can easily add a location.

I can pick if my post is public, followers only, or close friends.
