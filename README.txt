Building from Source
--------------------
We no longer release a source ZIP file because you need to use Subversion in 
order to get the v8 source code, so you may as well use it for the 
javascriptdotnet source too.


TODO - The previous instructions do not work any more. Need to write new ones.


Redistribution
--------------
Noesis.Javascript.dll needs the Microsoft C Runtime Libraries.
The exact version required is specified in a manifest file automatically
included inside the DLL.  You can extract it using 
MT.exe (from the Windows SDK):

> mt -inputresource:Noesis.Javascript.dll;2 -out:t.manifest
> type t.manifest

If you don't include the correct version of the runtime libraries
when you redistribute Noesis.Javascript.dll then you will get errors
when loading the DLL on some users machines.  (Many, but not all users
will already have it.)

Visual Studio 2010 is more flexible about where it finds its DLLs 
(http://mariusbancila.ro/blog/2010/03/24/visual-studio-2010-changes-for-vc-part-5/)
so you need not worry about the manifest, but you should still redistribute the
runtime library because the user may not have it.
