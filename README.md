# multivol - Submitted in 1985 to Usenix Archives.

Multi-volume tape archive

This app is really just a bit of nostalgia and reminisce from my days as a systems programmer at the University of Queensland Computer Science Department from 1985-1987. 


**Who knows maybe one day my children or theirs will stuble on it :)** ... *Hi - Glad you found it!* 

## My early computing days. 

This week my 9 year old son asked me to teach him Python so he could code 3D games in Blender. He also just published his first 40 videos on YouTube. Amazing!  As I was typing this he just dropped into my office and asked I could update his Blender software to the latest version. He's starting on a different planet to where I began my coding journey.

One of the first computer I used was owned by the Business School at Queensland University of Technology. It had 16kb of iron core memory and 30 character per second teletype which could also read and punch tape. The computer boasted a high speed optical paper tape reader. 

## My first and second full time jobs. 

In 1982 I had just graduated and took my first full-time job as a trainee programmer at the Queensland Electricity Generating Board (QEGB) which is now Energex. Most of the time I wrote and maintained Fortran for engineers and then eventually served my country writing COBOL for 3 months (which I loathed).
  
In 1984 I began swotting up on this new thing called "Unix" and reading Dennis Ritchie's "The C Programming Language" with zeal. In 1985 I departed from my QEGB job to work as a system programmer back at the computer science department at the University of Queensland where I had completed my Science degree.

Some from my old job thought me foolish to be departing from their safe mainframes to take up this "unproven" new platform called Unix. *"It will never be used commercially"* they told me ...  *"It's too insecure!"*. But I had learned that I could code in one line of shell script what took me hours on the ICL 2900 mainframe and I figured that in time it's weaknesses would be fixed. As it turned out, the UQ computer science department was also one of the best places in town to be part of the early Internet as at that time only academic and research institutions were permitted access. In 1985 there were just 2,000 computers online. Within four years there would be 200,000.  I think my change of job was a good call!  I chuckle sometimes thinking that the early shell script language and even occainsionally the "vi" text editor that I learned all those years ago I'm still using today on modern Macs, Windows and Linux when building modern cloud services. 

Multivol was probably my first software project on Unix. I tested it on floppy disks, reel to reel tapes and hard disk drums so we could backup and restore onto any removeable media.  We also tested it on multiple versions of Unix including Berkley 4.3 and System V. We mainly used it on the Perkin Elmer timeshare computer that served the needs of computer science staff and Dec PDP-11 machines used by our undergraduate students.

## Other Applications

During this job I wrote an offline archive system so anyone in the department who might be short on disk space could request that one or more of their directories be archived on to tape. The system would then schedule an archive operation to be run later in the week when our operator would mount the archive tapes. The app would store an index of the archived files under their home area so they could find and request archived files to be retrived.     

I also wrote my first distributed application that installed and configured disk quotas for students.  It read in their subject enrollments and from this computed their allocated disk quotas (each student had restricted disk space). It then generated new student account passwords which we printed out and issued at the Comp. Sci. School office. The app used a feedback loop to check that the changes pushed on the 3 computers (named **madvax1**, **madvax2** and **madvax3**) had been enacted. If there were any differences, it generated commmands required updated the differences and dispatched them in parallel to each host. This design ensured that any updates that failed (or even security breaches) would be automatically repaired. Years later, I used this same incremental update + feedback loop design to implement a system that migrated settings of Australia's analogue telephones to new digitial exchanges. 

## 1980's Fun

One year one of the lecturers decided to run a competition for the honors students to break the security of our Berkely Unix system. This was conducted on approval from the systems programmer team. The deal was that they had to create a file owned by them in a directory they did not have access to. They then had to subsequently document their method and reveal it to the systems programmers so we could fix it (we had full source code for the Berkley Unix and making fixes was encouraged). One student figured that he didn't know that much about Unix and so he decided to solve the problem a different way. So he approached one of the systems programmers and offered for some commensurate fee that he assist him in creating the required file ... so I greed!  I didn't take any money but  figured that he'd solved the problem :) .

On another occaison, one of our operators was using `multivol` to perform an incremental daily backup. Normally this would be a small backup set that would happly fit on one tape but this day multivol requested 17 tapes!! The reason? One enterprising student thought he'd show off to his fellow students how he'd managed to exceed his disk quota by a massive margin. To do this he wrote a small C app that performed a "seek()" call to an large offset in the file and then wrote a single block.  The resulting file was huge in size but due to the way that Unix stores files it was tiny in the actual number of blocks consumed (hence he'd not exceed his disk quota). 




