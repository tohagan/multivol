# multivol - Submitted in 1985 to Usenix Archives.

Multi-volume tape archive

This app is really just a bit of nostalgia and reminisce from my days as a systems programmer at the University of Queensland Computer Science Department from 1985-1987. 


**Who knows maybe one day my children or theirs will stuble on it :)** ... *Hi - Glad you found it!* 

## Family

This week my 9 year old son asked me to teach him Python so he could code 3D games in Blender. He also just published his first 40 videos on YouTube. Amazing!  As I was typing this he just dropped into my office and asked I could update his version of Blender.

## History

In 1982 I had just graduated and took my first full-time job at the Queensland Electricity Generating Board (QEGB) which is now Energex.  
  
In 1984 I was swotting up on this new thing called "Unix" and reading Dennis Ritchie's "The C Programming Language" with zeal. In 1985 I departed from my goverment job to work as a system programmer back at the computer science department at the University of Queensland where I had completed by Science degree.

Some from my old job though me foolish to be departing from their safe mainframes to take up this "unproven" new platform called Unix. *"It will never be used commercially"* they told me ...  *"It's too insecure!"*. But I has learned that I could code in one line of shell script what took me hours on the ICL 2900 mainframe and I figured that in time it's weaknesses would be fixed. As it turned out, the UQ computer science department was also one of the places in town to be to part of the early Internet as at that time only academic and research institutions were permitted access. In 1985 there were just 2,000 computers online. Within four years there would be 200,000.  I think my change of job was a good call!

Multivol was probably my first software project on Unix. I tested it on floppy disks, reel to reel tapes and hard disk drums so we could backup and restore onto any removeable media.  We also tested it on multiple versions of Unix including Berkley 4.3 and System 5. We mainly used it on the Perkin Elmer  

## Other Applications

During this job I wrote an offline archive system so anyone in the department who might be short on disk space could request that one or more of their directories be archived on to tape. The system would then schedule an archive operation to be run later in the week when our operator would mount the archive tapes. The app would store an index of the archived files under their home area so they could find and request archived files to be retrived.     

I also wrote my first distributed application that installed and configured disk quotas for students.  It read in their subject enrollments and from this computed their allocated disk quotas (each student had restricted disk space). It then generated new student account passwords which we printed out and issued at the Comp. Sci. School office. The app used a feedback loop to check that the changes pushed on the 2 computers (named **madvax1**, **madvax2** and **madvax3**) had been enacted. If there were any differences, it generated the commmands required to for each host to updated the differences. This design ensured that any updates that failed (or even security breaches) would be automatically repaired. Years later, I used this same incremental update + feedback loop design to implement a system that migrated settings of Australia's analogue telephones to new digitial exchanges. 

## 1980's Fun

One year one of the lecturers decided to run a competition for the honors students to break the security of our Berkely Unix system. This was conducted on approval from the systems programmer team. The deal was that they had to create a file owned by them in a directory they did not have access to. They then had to subsequently document their method and reveal it to the systems programmers so we could fix it (we had full source code for the OS and making fixes was encouraged).   One student figured that he didn't know that much about Unix and so he decided to solve the problem a different way. So he approached one of the systems programmers and offered for some commensurate fee that he assist him in creating the required file ... so I greed!  I didn't take any money but  figured that he'd solved the problem :) .




