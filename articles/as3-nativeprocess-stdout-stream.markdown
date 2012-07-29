Title: What I learned from AS3 NativeProcess output
Author: Aaron Fay
Date: Thu Jul 26 2012 09:52:00 GMT-0700 (PDT)
Node: v0.8.2

As I was hammering away on a project at my last job, I came across this issue
that plagued me for the longest time.  Normally I don't let uncaught exceptions
trickle up through my code, but in this case, I was being a bit complacent, mostly
because it wasn't obvious where the error was coming from, and frankly, I'm busy.

Well, it bit me in the ass finally, and I sat down for a few minutes to figure
out what the actual issue was.

### AS3 NativeProcess
I'm using NativeProcess to call a windows function to get some system information, 
like so:

    var file:File = File.resolvePath('cmd.exe'); // assume this is right there
    
