# Version Control and Cloud Storage Are Neat.

What we know as "the Internet" is really an incredibly complex development. At the end of 2018, the number of devices connected to the internet surpassed 22 Billion[^1]!

One of the most interesting things about how the internet has changed computing is that on the modern end-user desktop, nearly everything the user does is connected to some cloud service or another.

How many people keep music files on their drive anymore? Streaming from Spotify and Youtube are now the predominant ways of getting music.
Most people don't keep movies or games on disks anymore either, that has also been outsorced to services like Netflix, Disney+, Steam, or Xbox.

Even documents, and files that we place on our drives, are (often automatically) backed up with cloud storage solutions like OneDrive, I-Cloud, Dropbox, etc.

This of course comes with large amounts of controversy regarding privacy, user tracking, and data-ownership; although the amount of data the average computer user interacts with would quickly become cumbersome without all of this inter-connectivity. That, however, verges into it's own topic.

## Cloud Storage and File Sharing
Cloud storage is often something taken for-granted. There's a saying that states:

    "If your data doesn't exist in at least three places, it doesn't exist at all."

Cloud storage of course makes it easy to backup data in multiple, redundant, independent copies. 

Was your laptop stolen? Sign into your OneDrive and all your documents are still there!

Did your phone fall into a river while on a hike? I-Cloud has your pictures backed up! (Ideally)

But what if something happens to the cloud? (Or the cloud's copy of the data?)

## Version Control, Git, and Restic
Git is an industry standard in the world of software development. It tracks specific file changes within a folder over time, building a history of "commits" (changes to the files). If a current version of the files is lost or ruined, the user can simply revert back to and older commit. 

While designed for software development and programming, Git is also very handy for tracking changes in other files, and will keep track of any kind of file placed in it's repository (folder). Services like Github, Codeberg, and Gitlab even offer cloud-storage for these git-repositories! (Although they are by default public facing, so be aware of that.)

The tool and it's philosophy may be difficult for a new user to understand at first, but it becomes invaluable after overcoming the learning curve.

Restic is a program that will backup specified directories. It will copy, encrypt, and compress any set of folders and fils you like. It also functions very similar to Git, and I've found it to be very helpful for making broad system backups.

## The Point
As both a matter of privacy and of accesability, I prefer to have much more control over my files than the typical cloud provider would allow. I like to have local file-system access to the files I work on, but this leaves obvious problems with backups (only one copy!) and accesibility (I can't access from my phone!)

Using Git and private remote repositories, I've found the most ideal solution to date. Making the folder a git-repository, then pushing (uploading) it to a private remote repository, I can then clone (download) the repository to my phone or any other device. This leaves me with (by default) three copies: Computer, Phone, Remote-repo, and as many mirrors as I decide to set up. Keys can be created to controll access and sign each change so it becomes easier to verify the files that get shared between devices.

Not the simplest solution, and perhaps not the most elegant, but it has fit very well into my workflow so far.


[^1]: At least according to [HelpNetSecurity.com](https://www.helpnetsecurity.com/2019/05/23/connected-devices-growth/)

