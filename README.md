Shared Hosting File System
====

A distributed high availability filesystem targeted at shared hosting.

Many features are taken from OpenAFS, with specific features targeted at file hosting and short running scripts, like PHP.


Planned features:
Distributed - Files should be able to spread over multiple servers, and the same file replicated to other servers.

Replication - A Read/Write volume can be replicated to multiple Read only volumes in real-time(Constantly trying to cach up)
              It should also be possible to selectively replicate files, files under a certain file, files under a certain size etc.

Failover    - If a server containing a volume fails, the client will fail over to another replicated volume.
              If the failed volume is a R/W volume, it will only be possible to read files, and writes will fail.
              (Possibly, writes will be queued, or turn a read volume into a R/W)
              
Security    - Ability to create users and groups, and then assign permission for these on files and folders.
              Commands between servers are encrypted, data not necessarily.
              
Development Steps:
1. Proof of concept, learning run
  Develop a proof of concept without much of a plan, to see if it's possible to implements all the features, and
  to find potentional performance and development problems.
2. First development, not production ready
3. Second development, production ready


