UNIX

A HISTORY AND A MEMOIR

ALSO BY BRIAN KERNIGHAN

*The Elements of Programming Style* (with P. J. Plauger) *Software Tools* (with P. J. Plauger)

*Software Tools in Pascal* (with P. J. Plauger)

*The C Programming Language* (with Dennis Ritchie)

*The AWK Programming Language* (with Al Aho and Peter Weinberger)

*The Unix Programming Environment* (with Rob Pike)

*AMPL: A Modeling Language for Mathematical Programming* (with Robert Fourer and David Gay)

*The Practice of Programming* (with Rob Pike)

*D is for Digital*

*Hello, World: Opinion Columns from the Daily Princetonian The Go Programming Language* (with Alan Donovan)     *Understanding the Digital World*

*Millions, Billions, Zillions*

**UNIX**

**A Histor y and a Memoir**

**Brian Kernighan**

Kindle Direct Publishing

Copyright © 2020 by Brian W. Kernighan Published by Kindle Direct Publishing

www.kernighan.com All Rights Reserved

ISBN 978-169597855-3

Camera-ready copy for this book was produced by the author in Times Roman and Helvetica, using groff, ghostscript,

and other open source Unix tools.

Printed on acid-free paper. ∞         Printed in the United States of America 10  9  8  7  6  5  4  3  2  1

In memoriam DMR



**Contents**

**Preface** ix

**Chapter 1: Bell Labs** 1

1. Physical sciences at Bell Labs 5
1. Communications and computer science 7
1. BWK at BTL 8
1. Office space 11
1. 137 → 127 → 1127 → 11276  19

**Chapter 2: Proto-Unix (1969)** 27

1. A bit of technical background 27
1. CTSS and Multics 30
1. The origin of Unix 32
1. What’s in a name?  34
1. Biography: Ken Thompson 35

**Chapter 3: First Edition (1971)** 41

1. Unix for patent applications 42
1. The Unix room 45
1. The Unix Programmer’s Manual  49
1. A few words about memory 52
1. Biography: Dennis Ritchie 55

**Chapter 4: Sixth Edition (1975)** 61

1. File system  62
1. System calls  63
1. Shell 65
1. Pipes 67
1. Grep 70
1. Regular expressions  73
1. The C programming language 76
1. Software Tools and Ratfor 80
1. Biography: Doug McIlroy 82

viii  CONTENTS

**Chapter 5: Seventh Edition (1976-1979)** 87

1. Bourne shell  88
1. Yacc, Lex, Make 90
1. Document preparation  98
1. Sed and Awk  113
1. Other languages  117
1. Other contributions  121

**Chapter 6: Beyond Research** 131

1. Programmer’s Workbench  131
1. University licenses 134
1. User groups and Usenix 136
1. John Lions’ Commentary 137
1. Portability 140

**Chapter 7: Commercialization** 143

1. Divestiture  143
1. USL and SVR4 144
1. UNIX™ 146
1. Public relations  147

**Chapter 8: Descendants** 153

1. Berkeley Software Distribution  153
1. Unix wars  156
1. Minix and Linux 158
1. Plan 9 160
1. Diaspora 163

**Chapter 9: Legacy** 165

1. Technical  166
1. Organization  170
1. Recognition 175
1. Could history repeat? 177

**Sources** 181

**Preface**

“One of the comforting things about old memories is their tendency to take on a rosy  glow.  The  memory  fixes  on  what  was  good  and  what lasted, and on the joy of helping to create the improvements that made life better.”

Dennis Ritchie, “The Evolution of the Unix Time-sharing System,” October 1984

Since its creation in a Bell Labs attic in 1969, the Unix operating system has spread far beyond anything that its creators could possibly have imag- ined.  It has led to the development of much innovative software, influenced myriad programmers, and changed the entire path of computer technology.

Unix and its derivatives aren’t widely known outside a particular technical community, but they are at the heart of any number of systems that are part of everyone’s world.  Google, Facebook, Amazon, and plenty of other services are powered by Linux, a Unix-like operating system that I’ll talk about later on.  If you have a cell phone or have a Mac, it runs some version of Unix. If you have  gadgets like Alexa at home or navigation software in your car, they’re powered by Unix-like systems too. If you’re bombarded by advertis- ing whenever you browse the web, Unix systems are behind it, and of course the tracking that knows what you’re doing so you can be more accurately bombarded is likely to be based on Unix as well.

Unix was created more than 50 years ago by two people, along with a small group of collaborators and camp followers.  Through a sequence of lucky accidents, I was present at the creation, though certainly not responsi- ble for any of it.  At most I can take credit for a modest amount of useful software and, thanks to first-rate co-authors, some books that have helped

x PREFACE

people to learn more about Unix and its languages, tools and philosophy.

This book is part history and part memoir, a look at the origins of Unix and an attempt to explain what Unix is, how it came about, and why it mat- ters.  The book is certainly not a scholarly work, however—there are no foot- notes—and it has become less history and more memoir than I had originally planned.

The book is written for anyone with an interest in computing or the his- tory of inventions.  It includes a certain amount of technical material, but I’ve tried to provide sufficient explanation that even if you don’t have much back- ground, you can appreciate the basic ideas and see why they might be impor- tant.  You can safely skip over anything that seems too complicated, however, so there’s no need to read every word.  If you are a programmer, some of the explanations  may  seem  pretty  obvious  and  over-simplified, but  with  luck some of the historical insights will be useful, and the stories that go with it might be new and interesting to you.

Although I have tried to be accurate, there are sure to be places where my memory is imperfect. Furthermore, the interviews, personal reminiscences, oral histories, books and papers that I’ve relied on are not always consistent with my own memories or with each other in their accounts of who did what and when.

Fortunately, many of those involved in the early days are still alive and have helped to straighten me out. They too may suffer from memory lapses and rose-colored glasses but any errors that remain are my fault, at least until I can safely blame them on someone else.

My main purpose in writing is to tell some of the wonderful stories of an especially productive and formative time in the history of computing. It’s important to understand the evolution of the technology that we use and take for granted. The decisions that shaped how that technology developed and thus defined the paths that we took were made by real people, working under the pressures and constraints of the time. The more we know about the his- tory, the more we can appreciate the inventive genius that led to Unix and perhaps better understand why modern computer systems are as they are.  If nothing else, choices that might seem wrong-headed or perverse today can often be seen as natural consequences of what was understood and could be accomplished with the resources available at the time.

The story is about more than just the Unix operating system, though that’s the core. It also includes the C programming language, one of the most widely used of all languages, and at the heart of the systems that run the Internet and the services that use it. Other languages began life at Bell Labs with Unix too, notably C++, which is also widely used. Microsoft Office

PREFACE xi

tools like Word, Excel or Powerpoint are written in C++, as are most of the browsers you might be using. A dozen or two of the core tools that program- mers use daily and simply take for granted were written in the early days of Unix and are still part of every programmer’s toolkit, often much the same as they were 40 or 50 years ago.

Computer  science  theory  plays  a  vital  role  as  well,  often  enabling immensely practical tools. Hardware research explored design tools, inte- grated circuits, computer architecture, and unusual special-purpose devices. The interplay among all of these activities often led to unexpected inventions, and  was  one  of  the  reasons  why the  whole  enterprise  was  so  productive across so many different fields.

There is also an interesting and relevant story about how technological innovation happens. Bell Labs, where Unix began, was a remarkable institu- tion that produced many good ideas and capitalized on them. It was the ori- gin of many world-changing inventions, and there are lessons to be learned from how it worked.

The Unix story certainly offers many insights into how to design and build software, and how to use computers effectively, which I have tried to highlight along the way. As a simple but characteristic example, the Unix philosophy of software tools made it possible to combine existing programs to accomplish a wide variety of tasks without having to write new software. It’s a programming  instance  of  an  old  strategy:  divide  and  conquer. By breaking bigger tasks into smaller ones, each one becomes more manageable, and the pieces can be combined in unexpected ways.

Finally, although Unix was the most visible software from Bell Labs, it was by no means the only contribution to computing. The Computing Sci- ence Research Center, the fabled “Center 1127,” or just “1127,” was unusu- ally productive for two or three decades. Its work was inspired by Unix and used Unix as a base, but the contributions go well beyond that. Members of 1127 wrote important books that for years have been core texts in computer science and references for programmers. Center 1127 was an exceptionally influential industrial computer science research laboratory, one of the most productive of comparably sized groups at the time or subsequently.

Why was Unix and the surrounding environment so successful? How did a two-person  experiment  grow into  something  that  literally  changed  the world?  Was this a singular event, so unlikely that nothing like it could ever happen again?  On the larger question of whether such influential results can be planned, I’ll say more at the end of the book. For now, it seems to me that Unix owes its success to an accidental combination of factors: two excep- tional  people,  an  excellent  supporting  cast,  talented  and  enlightened

xii  PREFACE

management, stable funding in a corporation that took a very long view, and an unfettered environment for exploration no matter how unconventional.  Its adoption was facilitated by rapidly advancing technology where hardware kept getting smaller, cheaper and faster at an exponential rate.

The early years of Unix were for me and many others at Bell Labs won- drously productive and fun. I hope that this book will help you sense some of the joy of creation, and indeed of making life better, that Dennis Ritchie described in the epigraph above.

**Acknowledgments**

One of the unexpected pleasures of writing this book has been to recon- nect with so many friends and colleagues, who have generously shared their memories and some great stories. It is hard to express just how valuable that has been. I haven’t been able to include all of the stories, but I have greatly enjoyed hearing them, and I am in debt to the many remarkable people that I have been fortunate enough to work with.

Biographical material is scattered throughout the book, with major sec- tions on the three main people without whom Unix would not have hap- pened—Ken Thompson, Dennis Ritchie and Doug McIlroy.  Ken and Doug have provided invaluable feedback on the book, though they are in no way responsible for anything I’ve gotten wrong or inadvertently misrepresented. I have also received valuable comments and suggestions from Dennis’s broth- ers John and Bill; his nephew Sam provided detailed comments on several drafts.

As he has done so many times before, Jon Bentley gave me invaluable insights, helpful suggestions for organization and emphasis, numerous anec- dotes, and detailed comments on writing, over at least half a dozen drafts. I am enormously indebted to Jon once again.

Gerard Holzmann provided advice, archival material and many original photographs that have helped to make the book more visually interesting.

Paul Kernighan read multiple drafts and spotted myriad typos. He also suggested some excellent titles, though in the end I regretfully decided not to use *A History of the Unix-speaking Peoples.*

Al Aho, Mike Bianchi, Stu Feldman, Steve Johnson, Michael Lesk, John Linderman, John Mashey,  Peter Neumann, Rob Pike, Howard Trickey and Peter Weinberger provided critical reading and stories of early Unix days, many of which I have quoted or paraphrased.

PREFACE xiii

I also  received many helpful  comments  and  other  contributions  from Michael Bachand, David Brock, Grace Emlin, Maia Hamin, Bill Joy, Mark Kernighan, Meg Kernighan, William McGrath, Peter McIlroy, Arnold Rob- bins, Jonah Sinowitz, Bjarne Stroustrup, Warren Toomey and Janet Vertesi.

I am deeply grateful for all of the generous assistance, but I am responsi- ble for any errors or misinterpretations. Many other people have contributed to Unix in important ways over the past fifty years, and I apologize to anyone whose work has been slighted.



Chapter 1![](Aspose.Words.01dac56d-d681-4cb4-b03f-dcc548ac5921.001.png)

**Bell Labs**

“One Policy, One System, Universal Service”

AT&T’s mission statement, 1907

“At first sight, when one comes upon it in its surprisingly rural setting, the Bell Telephone Laboratories’ main New Jersey site looks like a large and up-to-date factory, which in a sense it is. But it is a factory for ideas, and so its production lines are invisible.”

Arthur Clarke, *Voice Across the Sea*, 1974

quoted in *The Idea Factory* by Jon Gertner, 2012

To  understand how Unix happened, we have  to understand Bell Labs, especially how it worked and the creative environment that it provided.

AT&T, the American Telephone and Telegraph Company,  grew out of combining  a  host  of  local  telephone  companies  from  across  the  United States.  Early in its history, AT&T realized that it needed a research organiza- tion that would systematically address the scientific and engineering prob- lems that the company encountered as it tried to provide a national telephone system.  In 1925, it created a research and development subsidiary, Bell Tele- phone Laboratories, to attack these problems. Although the full name was regularly abbreviated to Bell Labs or BTL or merely “the Labs,” telephony was always the central concern.

Bell Labs was originally located at 463 West Street in New York City, but at the beginning of the Second World War, many of its activities moved out of New York.  AT&T was heavily involved in the war effort, providing exper- tise on a wide variety of important military problems—communications sys- tems, of course, but also fire-control computers for anti-aircraft guns, radar, and cryptography.  Part of this work was done in suburban and rural New

` `CHAPTER 1: BELL LABS

![](Aspose.Words.01dac56d-d681-4cb4-b03f-dcc548ac5921.002.jpeg)

**Figure 1.1:** From New York City to Murray Hill, New Jersey

CHAPTER 1: BELL LABS 3

Jersey, 20 miles (33 km) west of New York.  The largest site was in an area called Murray Hill, which was part of the small towns of New Providence and Berkeley Heights.

Figure 1.1 shows the general lay of the land; 463 West Street is on the Hudson River, a short distance north of the 9A highway marker. Bell Labs at Murray Hill straddles the boundary between New Providence and Berkeley Heights, just north of Interstate 78. Both locations are marked on the map with dots.

More and more Bell Labs activities shifted to Murray Hill, and the Labs left West Street entirely in 1966. By the 1960s, Murray Hill housed over 3,000 people, at least 1,000 with PhDs in technical fields like physics, chem- istry, mathematics, and various flavors of engineering.

Figure 1.2 is an aerial photo of the Murray Hill complex in 1961.  There were three main buildings.  Building 1 is to the lower right in the picture, 2 is to the upper left, and 3 is the square one with an open courtyard. Before it was blocked by the addition of two new buildings in the 1970s, there was a single uninterrupted quarter-mile (400 m) corridor from one end of Building 1 to the other end of Building 2.

I spent over 30 years in Building 2, from an internship in 1967 until I retired in 2000. My offices were in the side wings marked with dots, on the fifth (top) floor. For future reference, Stair 9 in this picture is at the absolute far end of Building 2, and Stair 8 is one wing closer to the center. For most of the early years, the Unix room was in the sixth floor attic between stair- ways 8 and 9.

Figure 1.3 shows a Google satellite image of Bell Labs in 2019. Build- ings 6 (towards the lower left, with the marker) and 7 (towards the upper right) were added in the early 1970s, and for some years after 1996, Building 6 was the headquarters of Lucent Technologies.  It’s intriguing how much corporate history is captured in the labels that Google has assigned: “Bell Labs” as a marker, Lucent Bell Labs on the exit driveway,  Alcatel-Lucent Bell Labs on the entry, and Nokia Bell Labs at the apex of the managerial pyramid in Building 6.

I’m not qualified to write a detailed history of the Labs, but fortunately that’s already been done well by other writers. I particularly like Jon Gert- ner’s *The Idea Factory*, which focuses on the physical sciences, and James Gleick’s *The Information* is excellent for information science. The volumi- nous (seven volumes and nearly 5,000 pages) official Bell Labs publication called *A History of Science and Engineering in the Bell System* is thorough, authoritative, and in my sampling, always interesting.

` `CHAPTER 1: BELL LABS

![](Aspose.Words.01dac56d-d681-4cb4-b03f-dcc548ac5921.003.jpeg)

**Figure 1.2:** Bell Labs in 1961 (Courtesy of Bell Labs)

CHAPTER 1: BELL LABS 5

1. **Physical sciences at Bell Labs**

During its early years, most research at Bell Labs involved physics, chem- istry, materials, and communications systems. Researchers had exceptional freedom to pursue their own interests, but the environment was so rich in rel- evant problems that it wasn’t hard to explore in areas that were both scientifi- cally interesting and potentially useful to the Bell System and to the world at large.

Bell Labs was responsible for a remarkable number of scientific and tech- nological advances that changed the world.  Foremost among them was the transistor, invented in 1947 by John Bardeen, Walter Brattain and William Shockley, who were trying to improve amplifiers for long-distance telephone circuits.  The transistor resulted from fundamental research into the proper- ties of semiconductor materials, driven by a need for devices that would be more physically robust and less energy-hungry than vacuum tubes, which in the 1940s were the only way to make communications equipment and, inci- dentally, to build the earliest computers.

The  invention  of  the  transistor  was  recognized  with  a  Nobel  Prize  in physics in 1956, one of nine Nobel prizes that have been awarded to scien- tists for work done at least in part at Bell Labs. Other major inventions included negative feedback amplifiers, solar cells, lasers, cell phones, com- munications satellites and charge-coupled devices (which make the camera in your phone work).

Very roughly, in the 1960s through 1980s there were 3,000 people in the research area of Bell Labs (mostly at Murray Hill), and 15,000 to 25,000 in development groups in multiple locations that designed equipment and sys- tems for the Bell System, often using results from the research area. That’s a lot of people. Who paid for them all?

AT&T was effectively a monopoly, since it provided telephone service to most of the United States, but its ability to exploit its monopoly power was constrained.  It was regulated by federal and state bodies that controlled the prices that it could charge for its various services, and it was not allowed to enter businesses that were not directly related to providing telephone ser- vices.

This regulatory regime worked well for many years.  AT&T was required to provide service to everyone (“universal service”) no matter how remote or unprofitable.  As compensation, it got a stable and predictable overall rate of return.

As part of this arrangement, AT&T directed a small fraction of its revenue to  Bell  Labs,  with  the  express  purpose  of  improving  communications

` `CHAPTER 1: BELL LABS

![](Aspose.Words.01dac56d-d681-4cb4-b03f-dcc548ac5921.004.jpeg)

**Figure 1.3:** Bell Labs in 2019; Building 6 is towards the lower left

CHAPTER 1: BELL LABS 7

services.  In effect, Bell Labs was paid for by a modest tax on every phone call in the country. According to a paper by A. Michael Noll, AT&T spent about 2.8 percent of its revenues on research and development, with about 0.3 percent on basic research. I’m not sure how well this would work today, but for decades, the arrangement led to a steady flow of improvements to the phone system and a significant number of fundamental scientific discoveries. Stable funding was a crucial factor for research. It meant that AT&T could take a long-term view and Bell Labs researchers had the freedom to explore  areas  that  might  not  have  a  near-term  payoff and  perhaps  never would.  That’s a contrast with today’s world, in which planning often seems to look ahead only a few months, and much effort is spent on speculating about financial results for the next quarter.

2. **Communications and computer science**

Bell Labs was naturally a pioneer in designing, building and improving communications systems, a blanket term that covered everything from the design of consumer hardware like telephones through to the infrastructure of switching systems, microwave transmission towers, and fiber optic cables.

Sometimes this breadth of practical concerns could even lead to advances in basic science. For example, in 1964 Arno Penzias and Robert Wilson were trying to figure out what was causing unwanted noise in the antenna that Bell Labs was using to detect radio signals bounced off Echo balloon satellites.  They eventually deduced that the noise came from the background radiation that was the residue of the cosmic Big Bang at the beginning of the universe.  This discovery led to the 1978 Nobel Prize in physics for Penzias and Wilson.  (Arno says that “Most people get Nobels for things they were looking for. We got one for something we were trying to get rid of.”)

Another part of the Bell Labs mission was to develop a deep mathematical understanding of how communications systems worked.  The most important result was Claude Shannon’s creation of information theory, which was in part motivated by his study of cryptography during World War II. His 1948 paper “A Mathematical Theory of Communication,” published in the *Bell System Technical Journal*, explained the fundamental properties and limita- tions on how much information could be sent through a communications sys- tem.  Shannon worked at Murray Hill from the early 1940s to 1956, then returned to teach at MIT, where he had been a graduate student. He died in 2001 at the age of 84.

As computers became more powerful and less expensive, computer use expanded to include more data analysis, along with extensive modeling and

` `CHAPTER 1: BELL LABS

simulation of physical systems and processes. Bell Labs had been involved with computers and computing since the 1930s, and had computer centers with big central computers by the late 1950s.

In the early 1960s, a computer science research group was formed by splitting some people out of mathematics research, along with some of the staff who operated the large central computer at Murray Hill. The resulting amalgam was called the Computing Science Research Center, and although for a brief period it still ran computer services for all of Murray Hill, it was part of the research division, not a service function. In 1970 the group that managed the computer facilities was moved into a separate organization.

3. **BWK at BTL**

This section contains a fair amount of personal history, which I hope will give you some idea of the lucky accidents that led me to computing as a career, and to Bell Labs as an unequaled place to pursue it.

I was born in Toronto, and went to the University of Toronto.  I was in a program called Engineering Physics (later renamed to Engineering Science), a catch-all program for those who didn’t really know what they wanted to focus on. I graduated in 1964, which was in the early days of computing: I saw my first computer when I was in my third year at university. There was only one big computer for the whole university, an IBM 7094, which was pretty much top of the line. It had 32K (32,768) 36-bit words of magnetic core memory (today we would say 128K bytes), and some secondary storage in the form of big mechanical disk drives.  It cost literally three million US dollars at the time and it lived in a large air-conditioned room, tended by pro- fessional operators; ordinary people (and especially students) did not get any- where near it.

As a result, I did little computing as an undergraduate, though I did try to learn the Fortran programming language. For anyone who has ever struggled to write their first program, I can sympathize. I studied Daniel McCracken’s excellent book on Fortran II and had the rules down pat, but I couldn’t figure out how to write that first program, a conceptual barrier that many people seem to encounter.

In the summer before my final year of college, I landed a job at Imperial Oil in Toronto, in a group that developed optimization software for refineries. (Imperial  Oil  was  partly  owned  by  Standard  Oil  of  New Jersey,  which became Exxon in 1972.)

In retrospect, I was well below average as an intern. I spent the entire summer trying to write a giant Cobol program for analyzing refinery data. I

CHAPTER 1: BELL LABS 23

don’t recall its precise purpose, but I know for sure that it never worked.  I didn’t really know how to program, Cobol provided little support for good program organization, and structured programming had not been invented, so my code was an endless series of IF statements that branched off somewhere to do something once I had figured out what that something should be.

I also tried to get Fortran programs running on Imperial’s IBM 7010, since I sort of knew Fortran, certainly better than I knew Cobol, and Fortran would have been better suited for data analysis. It was only after weeks of fighting JCL, IBM’s Job Control Language, that I deduced that there was no Fortran compiler on the 7010, but the JCL error messages were so inscrutable that no one else had figured that out either.

When I returned to school for my senior year after this somewhat frustrat- ing summer, I was still strongly interested in computing. There were no for- mal courses on computer science, but I did write my senior thesis on artificial intelligence,  a  hot  topic  at  the  time. Theorem  provers,  programs  to  play chess and checkers, and machine translation of natural languages all seemed like they were within reach, just requiring a bit of programming.

After graduating in 1964, I had no clue what to do next, so like many stu- dents I put off the decision by going to graduate school. I applied to half a dozen schools in the United States (not common among Canadians at the time), and by good luck was accepted by several, including MIT and Prince- ton.  Princeton said that the normal time to complete a PhD was three years, while MIT said it would probably take seven years.  Princeton offered a full fellowship; MIT said I would have to be a research assistant for 30 hours a week.  The decision seemed pretty clear-cut, and a good friend, Al Aho, who had been a year ahead of me at Toronto, was already at Princeton, so off I went.  It turned out to be an incredibly fortunate choice.

In 1966, I got lucky again, with a summer internship at MIT, thanks in part to the fact that another Princeton grad student, Lee Varian, had done a great job there in 1965. I spent the summer using CTSS, the Compatible Time-Sharing  System,  writing  programs  in  MAD  (Michigan  Algorithm Decoder, a dialect of Algol 58) to build tools for a new operating system called Multics, which we’ll come to in Chapter 2. (Multics was originally spelled MULTICS, but the lower-case version is less visually jarring; as with UNIX versus Unix and some other all-caps words, I’ll use the nicer-looking form even though it’s not historically accurate.)

My nominal boss at MIT was Professor Fernando Corbató, “Corby” to everyone, a wonderful gentleman, the creator of CTSS, and the person in charge of Multics. Corby won the Turing Award in 1990 for his fundamental work on time-sharing systems. He died in July 2019 at the age of 93.

In addition to leading the design and implementation of CTSS and Mul- tics, Corby was the inventor of passwords for computer access. There had been little need for such a thing with batch computing, but some security mechanism was necessary to protect private files on a time-sharing computer with a shared file system.

I still remember both of the short pronounceable passwords that were automatically generated for me while I was at MIT in the summer of 1966. Tw o passwords were needed, not one, because one day during the summer a mixup caused the file that stored the passwords to be exchanged with the file that held the login message of the day. Since passwords were stored unen- crypted, everyone who logged in got to see everyone else’s passwords.

My office, which I remember as being unshared, belonged to Professor Joseph  Weizenbaum,  but  he  was  away for  the  summer. Early  in  1966, Weizenbaum had published a description of Eliza, a program that simulated a dialog with a Rogerian psychologist. Eliza was one of the first attempts at using natural language to interact with a computer. It was surprisingly effec- tive, at least when first encountered, and I enjoyed showing it off to visitors. There are plenty of Eliza simulators on the web today; it’s still entertaining to play with them for a few minutes, though their weaknesses quickly become evident.

ELIZA: Please tell me what’s been bothering you. YOU:  I’m trying to write a book about Unix. ELIZA: Is it because you are trying to write a book

about unix that you came to me?

YOU:  Yes.

ELIZA: You are sure.

YOU:  Yes.

ELIZA: You seem to be quite positive.

YOU:  Yes.

ELIZA: I see.

In the summer of 1967, I got the ultimate piece of good luck: an intern- ship at Bell Labs in Murray Hill, in the Computing Science Research Center, working for Doug McIlroy (Figure 1.4). Doug suggested that I explore some problem in evaluating memory allocators, one of his long-term interests. In the  best  intern  tradition,  I  bumbled  around  and  eventually  did  something completely different, creating a library of functions that made it convenient to do list processing in Fortran programs. I spent the summer writing tight assembly language for the then-current big computer at Murray Hill, a GE 635, which was in effect a cleaned-up and more orderly IBM 7094, but also a simpler version of the GE 645 that had been specially designed for Multics. That’s pretty much the last time I wrote assembly language, but even though

what I was doing was fundamentally misguided, it was a blast and it hooked me completely on programming.

![](Aspose.Words.01dac56d-d681-4cb4-b03f-dcc548ac5921.005.jpeg)

**Figure 1.4:** Doug McIlroy, ∼1981 (Courtesy of Gerard Holzmann)

4. **Office space**

Sometimes geography is destiny.

My office as an intern in 1967 was on the fifth floor of Building 2, on a corridor off Stair 8. On my first day on the job, I was sitting in my office (the good old days when even an intern could luck into a private office), wonder- ing what to do, when an older guy appeared in my doorway at 11AM, and said “Hi, I’m Dick [unintelligible]. Let’s go to lunch.”

OK,  I  thought,  why not?  I don’t remember  anything  at  all  about  the lunch,  but  I  do  remember  that  afterwards,  Dick  [unintelligible]  went  off somewhere else, and I sneaked along the corridor to read the name tag on his door. Richard Hamming! My friendly next-door neighbor was famous, the inventor  of  error-correcting  codes,  and  the  author  of  the  textbook  for  a numerical analysis course that I had just taken.

Dick (Figure 1.5) became a good friend. He was a man of strong opinions and not afraid to express them, which I think put off some people, but I enjoyed his company and over the years profited a great deal from his advice. He was a department head, but there were no people in his department, which seemed odd. He told me that he had worked hard to achieve this com- bination  of  suitable  title  without  responsibility, something  that  I  came  to

appreciate only much later when I became a department head with a dozen people in my department.

![](Aspose.Words.01dac56d-d681-4cb4-b03f-dcc548ac5921.006.png)

**Figure 1.5:** Dick Hamming, ∼1975, in his trademark plaid jacket (Wikipedia)

I was there in the summer of 1968 when he learned that he had won the ACM Turing Award, which today is considered the computer science equiv- alent of a Nobel prize. Dick’s sardonic reaction: since the Nobel prize was at that time was worth $100,000 and the Turing award was worth $2,000, he said that he had won 2 percent of a Nobel prize. (This was the third Turing award; the first two went to Alan Perlis and Maurice Wilkes, also pioneers of computing.)  Dick was cited for his work on numerical methods, automatic coding systems, and error-detecting and error-correcting codes.

Dick was the person who started me writing books, which has turned out to be a good thing. He had a fairly low opinion of most programmers, who he felt were poorly trained if at all. I can still hear him saying

“We give them  a  dictionary  and  grammar  rules,  and  we  say, ‘Kid, you’re now a great programmer.’ ”

He felt that programming should be taught as writing was taught. There should be a notion of style that separated poor code from good code, and pro- grammers should be taught how to write well and appreciate good style.

He and I disagreed on how this might be accomplished, but his idea was sound, and it led directly to my first book, *The Elements of Programming Style*, which I published in 1974 with P. J. “Bill” Plauger, who was at the time  in  the  adjacent  office.  Bill and  I  emulated  Strunk  and  White’s *The*

*Elements of Style* by showing a sequence of poorly written examples, and explaining how to improve each of them.

Our first example came from a book that Dick had showed me. He came into my office one day carrying a numerical analysis text, all up in arms about how bad the numerical parts were. I saw only an awful chunk of For- tran:

DO 14 I=1,N

DO 14 J=1,N

14 V(I,J)=(I/J)\*(J/I)

If you’re not a Fortran programmer, let me explain.  The code consists of two nested DO loops, both ending at the line which has the label 14. Each loop steps its index variable from the lower limit to the upper limit, so in the outer loop I steps from 1 to N, and for each value of I, in the inner loop J steps from 1 to N. The variable V is an array of N rows and N columns; I loops over the rows and for each row, J loops over the columns.

This specific pair of loops thus creates an N by N matrix with 1’s on its diagonal and 0’s everywhere else, like this when N is 5:

1 0 0 0 0 0 1 0 0 0 0 0 1 0 0 0 0 0 1 0 0 0 0 0 1

The code relies on the fact that integer division in Fortran truncates any frac- tional part, so if I is not equal to J, one of the divisions will produce 0, but if I equals J (as it does on the diagonal), the result will be 1.

This all seemed way too clever to me, and misplaced cleverness is a bad idea in programming.

Rewriting it in a straightforward and obvious way leads to a clearer ver- sion: each time through the outer loop, the inner loop sets every element of row I to 0, and then the outer loop sets the diagonal element V(I,I) to 1:

C MAKE V AN IDENTITY MATRIX

DO 14 I = 1,N

DO 12 J = 1,N

12  V(I,J) = 0.0

14  V(I,I) = 1.0

This also led to our first rule of programming style:

*Write clearly—don’t be too clever.*

Dick retired from Bell Labs in 1976 and went to the Naval Postgraduate School in Monterey, California, where he taught until his death early in 1998 at the age of 82. The story goes that one of his courses there was known to students as “Hamming on Hamming,” which suggests an awkward parallel with this section of the book.

Dick thought hard all the time about what he was doing and why.  He often said that “The purpose of computing is insight, not numbers,” and he even had a tie with that written on it (in Chinese). One of his early insights was that computing would come to account for half the work at Bell Labs. None of his colleagues agreed, but in fact his estimate soon proved too con- servative. He used  to  say  that  Friday  afternoons  were  for  thinking  great thoughts, so he sat back and thought, though he was always welcoming to visitors like me at any time.

A few years after his retirement, Dick gave an insightful talk that distilled his  advice  on  how to have a successful  career, called  “You  and  Your Research,” which you can find on the web. He gave the first version of that talk at Bellcore in March 1986; Ken Thompson drove me there so we could hear it. I’ve been recommending the talk to students for decades—it really is worthwhile to read the transcript, or to watch one of the video versions.

Right across the hall from me in the summer of 1967 was Vic Vyssotsky (Figure 1.6), another incredibly smart and talented programmer. Vic was in charge of the Bell Labs part of Multics, a partner with Corby, but he still managed to find time to talk almost daily to a lowly intern. Vic pressed me into teaching a Fortran class to physicists and chemists who needed to learn how to program.  The experience of teaching non-programmers turned out to be good fun. It got me over any fear of public speaking and made it easy to get into a variety of teaching gigs later on.

Shortly afterwards, Vic moved to another Bell Labs location where he worked  on  the  Safeguard  anti-missile  defense  system. He  eventually returned to Murray Hill and became the executive director responsible for computer science research, and thus was my boss a couple of levels up.

By the spring of 1968, I had started to work on a problem for my PhD thesis, one suggested by my advisor, Peter Weiner. The problem was called *graph partitioning*: given a set of nodes connected by edges, find a way to separate the nodes into two groups of equal size such that the number of edges that connect a node in one group to a node in the other group is as small as possible. Figure 1.7 shows an example: any other partition of the nodes into two groups of five requires more than two edges between the two sets.

![](Aspose.Words.01dac56d-d681-4cb4-b03f-dcc548ac5921.007.png)

**Figure 1.6:** Vic Vyssotsky, ∼1982 (Courtesy of Bell Labs) 1 6![](Aspose.Words.01dac56d-d681-4cb4-b03f-dcc548ac5921.008.png)

2~~ 3~~ 7~~ 8

4~~ 5 9 10 **Figure 1.7:** Graph partitioning example

This was ostensibly based on a practical problem: how to assign parts of a program to memory pages such that when the program was run, the amount of swapping of program pages into and out of memory would be minimized. The nodes represented blocks of code, the edges represented possible transi- tions from one block to another, and each edge could have a weight that mea- sured the frequency of the transition and thus how costly it would be if the two blocks were in different pages.

It was an artificial problem in a way, but it was a plausible abstraction of something  real,  and  there  were  other  concrete  problems  that  shared  this abstract model. For example, how should components be laid out on circuit boards to minimize the expensive wiring that connected one circuit board to another?  Less plausibly, how might we assign employees to floors of a build- ing to keep people on the same floor as the people they talk to most often?

This was enough justification for a PhD thesis topic, but I wasn’t making much progress. When I returned to the Labs for a second internship in the summer of 1968, I described the problem to Shen Lin (Figure 1.8), who had recently developed the most effective known algorithm for the classic Travel- ing Salesman problem: given a set of cities, find the shortest route that visits each city exactly once, and then returns home.

Shen came up with an approach for graph partitioning that looked promis- ing, though there was no assurance that it would produce the best possible answers, and I figured out how to implement it efficiently. I did experiments on a large number of graphs to assess how well the algorithm worked in prac- tice.  It seemed highly effective, but we never discovered a way to guarantee an optimum solution. I also found a couple of interesting special-case graphs where I could devise algorithms that were both fast and guaranteed to pro- duce optimal solutions. The combination of results was enough for a thesis, and by the end of the summer I had everything I needed. I wrote it up over the fall, and had my final oral exam late in January 1969. (Princeton’s opti- mistic estimate of three years had turned into four and a half.)

A week later, I started work in the Computing Science Research Center at Bell Labs. I never had an interview; the Labs sent me an offer sometime in the fall, though with a caveat: my thesis had to be finished. Sam Morgan, the director of the Center and thus my boss two levels up, told me, “We don’t hire PhD dropouts.” Finishing the thesis was definitely a good thing; I got another letter in December saying that I had received a substantial raise, well before I reported for work!

As an aside, although Shen and I didn’t know it at the time, there was a reason why we were unable to find an efficient graph-partitioning algorithm that would always find the best possible answer. Others had been puzzling over the inherent difficulty of combinatorial optimization problems like graph partitioning, and had discovered some interesting general relationships.

In a remarkable 1971 result, Stephen Cook, a mathematician and com- puter scientist at the University of Toronto, showed that many of these chal- lenging problems, including graph partitioning, are equivalent, in the sense that if we could find an efficient algorithm (that is, something better than try- ing all possible solutions) for one of them, that would enable us to find effi- cient algorithms for all of them. It’s still an open problem in computer sci- ence whether such problems are truly hard, but the betting is that they are. Cook received the 1982 Turing Award for this work.

When I got to Bell Labs as a permanent employee in 1969, no one told me what I should work on. This was standard practice: people were introduced to other people, encouraged to wander around, and left to find their own

![](Aspose.Words.01dac56d-d681-4cb4-b03f-dcc548ac5921.009.jpeg)

**Figure 1.8:** Shen Lin, ∼1970 (Courtesy of Bell Labs)

research topics and collaborators. In retrospect, this seems like it must have been daunting, but I don’t recall any concern on my part. There was so much going on that it wasn’t hard to find something to explore or someone to work with, and after two summers I already knew people and some of the current projects.

This  lack  of  explicit  management  direction  was  standard  practice. Projects in 1127 were not assigned by management, but grew from the bot- tom up, coalescing a group of people who were interested in a topic. The same was true for work with other parts of the Labs: if I was involved with some development group, I might try to entice research colleagues to join me, but they would be volunteers.

In any case, for a while I continued to work with Shen on combinatorial optimization.  Shen was exceptionally insightful on such problems, able to sense a promising line of attack by playing with small examples by hand. He had a new idea for the traveling salesman problem, a technique that greatly improved on his previous algorithm (which was already the best known), and I implemented it in a Fortran program. It worked well, and for many years was the state of the art.

This kind of work was fun and rewarding, but although I could convert ideas into working code pretty well, I wasn’t any good at the algorithmic parts.  So I gradually drifted into other areas: document preparation software, specialized programming languages, and a bit of writing.

I did come back to work with Shen a couple of other times, including a complex tool for optimizing the design of private networks for AT&T cus- tomers.  It was good to flip back and forth between comparatively pure com- puter science and systems that were actually of some use to the company.

![](Aspose.Words.01dac56d-d681-4cb4-b03f-dcc548ac5921.010.jpeg)

**Figure 1.9:** PR photo, ∼1970 (Courtesy of Bell Labs)

The Bell Labs public relations operation was fond of Shen’s work on the Traveling Salesman problem and he figured in a number of advertisements. Figure 1.8 is a blurry excerpt from one of them, with me in the corner, and Figure  1.9,  from  some  glossy  PR  magazine  published  by  the  Labs,  talks about our work on graph partitioning, perhaps after we obtained a patent for the algorithm.

Note that, most uncharacteristically, I am wearing a tie. A few years later, Dennis Ritchie and I wrote an article about C for another company magazine, probably the *Western Electric Engineer*. Before publication, we were asked to send pictures of ourselves to accompany the article, which we did. After a few weeks, we were told that the pictures had been lost. No problem, we said, we can send them again.  To which the response was “This time, could you wear ties?” We replied with a firm no, and shortly afterwards the maga- zine was published with our original tie-less pictures, which had miracu- lously been found.

When I started as a permanent employee, my office was on the fifth floor of Building 2 on a corridor off Stair 9, and I stayed in it for 30 years, a fixed point in a world of change. Over the years, my neighbors across the hall included Ken Thompson, Dennis Ritchie, Bob Morris, Joe Ossanna, and Ger- ard Holzmann, and eminent visitors like John Lions, Andy Tanenbaum and David Wheeler.

For the last decade of my time at the Labs, Ken Thompson and Dennis Ritchie’s offices were directly across the corridor from mine. Figure 1.10 is a view of Dennis’s office, taken in October 2005 from my old office doorway. Ken’s office was to the left.

Over the years my immediate neighbors included Bill Plauger, Lorinda Cherry, Peter Weinberger and Al Aho. Doug McIlroy,  Rob Pike and Jon

![](Aspose.Words.01dac56d-d681-4cb4-b03f-dcc548ac5921.011.jpeg)

**Figure 1.10:** Dennis Ritchie’s office in 2005

Bentley were just a few doors away.  It’s easier to collaborate with people who are physically close; I’ve been truly lucky in my neighbors.

5. **137** → **127** → **1127** → **11276**

Who were the players at this time, and what was the environment like?  In the  early  1970s,  there  were  just  over 30 people  in  Computing  Science Research, with perhaps 4 to 6 working on Unix or things closely related to it. Figure 1.11 is a montage of part of the Bell Labs internal phone book. It’s not yellowed with age; when I arrived, the org chart part was printed on yel- low paper, just like the yellow pages in old telephone books.

The page is from 1969. It shows the Computing Science Research Center under Sam Morgan (Figure 1.12), who was an excellent applied mathemati- cian and an expert in communications theory. Doug McIlroy, who played an enormously important but not widely known role in Unix, managed a group that included Ken Thompson and others who were involved in early Unix, like Rudd Canaday, Bob Morris, Peter Neumann and Joe Ossanna. Elliot Pinson’s department  included  Dennis  Ritchie,  Sandy  Fraser  and  Steve

![](Aspose.Words.01dac56d-d681-4cb4-b03f-dcc548ac5921.012.jpeg)

**Figure 1.11:** Bell Labs phone book, ∼1969 (Courtesy of Gerard Holzmann)

Johnson, who were also part of Unix for many years.

Although most researchers had PhDs, no one used “Doctor”; it was first names for everyone.  One visible exception about titles was that in the phone book of Figure 1.11, women were either Miss or Mrs, while men were free of marital status indicators. I don’t recall exactly when this labeling stopped, but it was certainly gone from the phone book by the early 1980s.

In the 1960s and 1970s there were few women and people of color in technical positions at Bell Labs; most members of technical staff were white males, and it stayed that way for a long time. In this respect, the Labs was representative of most technical environments at this period in the history of computing.

During the early 1970s, Bell Labs started three long-running programs that attempted to improve the situation. The Cooperative Research Fellow- ship Program (CRFP) began in 1972; each year, it funded four years or more of graduate school for about 10 minority students to obtain their PhDs. The Graduate Research Program for Women (GRPW), which started in 1974, provided the same graduate school support for women, perhaps 15 or 20 per year. Several of them worked in Center 1127 and in my department at one

![](Aspose.Words.01dac56d-d681-4cb4-b03f-dcc548ac5921.013.png)

**Figure 1.12:** Sam Morgan, director of 1127, ∼1981 (Courtesy of Gerard Holzmann)

time or another, and most went on to successful careers within Bell Labs, at universities and at other companies. Each year, the Summer Research Pro- gram (SRP), also started in 1974, provided fully funded summer internships for  roughly  60  undergraduate  women  and  minority  students,  who  were hosted at Murray Hill, Holmdel and sometimes other locations, working one- on-one with a research mentor. I was in charge of SRP for Center 1127 for over 15 years, so I got to meet a lot of nice sharp undergrads, and mentor a few.

These programs were effective in the long run, but the environment was still quite homogeneous during the 1960s and 1970s, and I’m sure that I was oblivious to some of the issues that this raised.

Bell Labs had a clear managerial hierarchy.  At the top was the president, in charge of perhaps 15 to 25 thousand people. Beneath that were areas num- bered 10 (research), 20 (development), 50 (telephone switching), 60 (military systems), and so on, each with a vice president. Research itself was divided into physics (11), mathematics and communications systems (13), chemistry (15) and the like, with an executive director for each; it also included legal and patent groups. Mathematics Research was 131, and Computing Science Research was “Center 137,” with half a dozen individual departments like 1371.  In a major shift, all of this was renumbered a few years later, when we became Center 127, and then during some reorganization, an extra digit was added to the front, and we became 1127, a number that lasted until 2005,

well after I retired in 2000.

There were relatively few levels in the hierarchy.  Researchers like me were “member of technical staff” or MTS, and there were a couple of techni- cal levels below that.  MTS in Research normally got a private office, though everyone was expected to keep the door open most of the time. There was a supervisor level above this, though 1127 had only a few supervisors over the years.  The next level was department head, a person like Doug McIlroy who was responsible for half a dozen to a dozen individual researchers. The level above that was director of a center, who might have half a dozen depart- ments, then executive director, with a handful of centers, and then vice presi- dent, who oversaw the executive directors.

Vice  presidents  reported  to  the  president. Bill  Baker, an outstanding chemist, was vice president of research from 1955 until 1973, and president of Bell Labs until 1980. While he was vice president, it was believed that he knew every MTS in research by name and was aware of what they were working on. I think it might well have been true; certainly he always knew what my colleagues and I were up to.

I was a regular MTS until 1981, when I finally succumbed to the pressure to become a department head. Most people went into management reluc- tantly, because although it was not the end of personal research, it did repre- sent a slowdown, and it came with responsibilities like looking after one’s department that could be challenging. Of course the usual arguments were trotted  out:  “It’s inevitable,  why not  now?”  Or, somewhat  contradictory, “This might be your last chance.” Or, “If not you, it will be someone else not as good.”

For better or worse, I became head of a new department, 11276, with the carefully meaningless name “Computing Structures Research.” The depart- ment usually had 8 to 10 people with a daunting spectrum of interests: graph- ics hardware, integrated circuit design tools, document preparation, operating systems, networking, compilers, C++, wireless system design, computational geometry, graph  theory, algorithmic  complexity, and  lots  more  besides. Understanding what each of them was working on well enough to explain it further up the chain was always a challenge, though it was also rewarding, and a surprising amount of what I learned then has stuck with me.

The  management  hierarchy was  accompanied  by  a  few perks  at  each level.  Some were obvious, like successively bigger offices at director and above. I think there was also a modest salary increase for department heads but it certainly wasn’t big enough to be memorable.

Some were more subtle: department heads and up had carpeted offices, while ordinary folk had bare linoleum or vinyl tile. When I was promoted, I was given a glossy printed brochure listing my options for carpet color, office furniture, and the like.  I briefly tried a new desk but it was too big and uncomfortable, so I went back to the ancient Steelcase that I had inherited in 1969.  And I declined the carpet entirely, since I wasn’t enthusiastic about distinctions of rank. Sam Morgan advised me strongly that I should take the carpet.  He said that some day I would want the authority that came from having a carpet. I still declined, and the carpet distinction eventually went away.

The primary annual task for department heads was to assess the work of their department members in an elaborate ritual called “merit review.” Once a year each MTS wrote down on one side of one piece of paper a summary of what they had done during the year; in 1127, it was known as an “I am great report,” a term that I think originated with Sam Morgan.  The department head wrote another piece of paper that summarized and assessed the work, including “areas for improvement,” a section that was meant to contain con- structive criticism.

Writing the assessment and feedback was hard work, and there was a strong tendency to leave the areas for improvement part blank, but one year we were told that it had to be filled in; evasions like leaving it empty or say- ing “N/A” were no longer acceptable. I came up with the phrase “Keep up the good work,” and got away with that for a year or two before being told that more critical comments were required, on the grounds that no one was perfect.  Fortunately I didn’t have to do this for a star like Ken Thompson. What could one have said?

The department heads and the director met to come up with a consensus evaluation for each MTS. This normally took a full-day meeting. It was fol- lowed some weeks later by another full-day meeting that determined next year’s salaries by allocating each MTS a share of a pot of raise money.  These two related  evaluations  were  officially known  as  merit  review and  salary review, but I always thought of them as “abstract merit” and “concrete merit.”

This process was repeated up the management chain, with an executive director  reviewing  all  the  MTS  results  with  directors,  and  also  assessing department heads.

Although merit review in some centers could be competitive, our reviews were remarkably collegial.  Rather than “My people are better than your peo- ple,” the tone was more like “Don’t forget this other good work that your per- son did.”

I may be too sanguine, but I think the whole process worked well, because management was technically competent all the way up and everyone had gone through the process at lower levels.  The system did not seem to have much  of  a  bias  towards  either  practice  or  theory, at least  for  us  in 1127—good programs and good papers were both valued.  The absence of proposals or plans for future work was a good thing. One was expected to have roughly a year’s worth of accomplishments at the end of the year, but any number of false starts could be ignored, and management took a long view of people who worked on the same thing for multiple years. I think that it also helped that in Research there were very few management levels, so promotion wasn’t really on most people’s radar most of the time. If one really aspired to be a manager, an organization outside of Research would likely be a better option.

It’s interesting to compare the Bell Labs evaluation process with how it’s done in research universities.  In the latter, hiring and especially promotion are strongly influenced by a dozen or more letters solicited from prominent outside researchers who are in the same specialty. This tends to encourage deep expertise in narrow fields, since the goal of a reviewee is to master some field so well that external reviewers can legitimately say “This person is the best person in this sub-field at this stage of his or her career.”

By contrast, Bell Labs created a rank order for every researcher, from the bottom up. Each department head ranked his or her people; those rankings were merged by department heads within a center, and those in turn by the next two levels, so by the end everyone’s approximate position in the whole population was determined.

A person who did great work in a narrow field might well be ranked highly by his or her immediate management, but no one further up would likely know of the work.  Interdisciplinary work, on the other hand, stood out at higher levels because more managers would have seen it. The broader the collaborations, the more managers would know about it. The end result was an  organization  that  strongly  favored  collaboration  and  interdisciplinary research.  And because the managers who made the decisions had come up through the same process, they were inclined in the same direction.

I was a department head for over 15 years, was probably at best an aver- age manager, and was definitely happy to step down.  Others successfully resisted promotion for long periods; Dennis Ritchie became a department head well after I did, and Ken Thompson never did.

Having now taught at a university for 20 years, I’m still not enthusiastic about sitting in judgment on other people’s work.  It’s necessary, however, and sometimes one has to make decisions that do affect people’s lives, like firing someone (which I fortunately never had to do) or failing a student in a course (not common but not unheard of either). One of the good things about the Bell Labs process was that it was based on the shared judgment of other

CHAPTER 1: BELL LABS 25

people who understood the work.  As Doug McIlroy said, “Collegiality was the genius of the system. Nobody’s advancement depended on the relation- ship with just one boss.” The process at the Labs wasn’t perfect, but it was pretty good and I’ve certainly heard and read about performance review pro- cesses that are far worse.



