## Building for multiple game versions

This fork is designed to handle multiple client specific TOC files.

- Retail
  1. AddOnName_Mainline.toc
  2. AddOnName-Mainline.toc
  3. AddOnName.toc

- BCC
  1. AddOnName_TBC.toc
  2. AddOnName_BCC.toc
  3. AddOnName-TBC.toc
  4. AddOnName-BCC.toc
  5. AddOnName.toc

- Classic Era
  1. AddOnName_Vanilla.toc
  2. AddOnName_Classic.toc
  3. AddOnName-Vanilla.toc
  4. AddOnName-Classic.toc
  5. AddOnName.toc


While you do not require an AddOnName.toc if you have an AddOnName-Mainline.toc
file, some hosting services (eg CurseForge) cannot handle that situation and you
may be better off leaving it as the default format.

Use of the -g option should not be required, and is untested so i have no idea
what it will do, so dont use it.

All you need to do is setup toc files for the clients that your addon supports (with
the appropriate interface versions in them) and a single zip file will be built, uploaded,
and tagged for each of the interface versions that the hosting site accepts.

note - some of the hosting sites do not support all interface versions.
Where they do not support a specific interface version you have set then that
version will be removed from the upload and you will receive a warning,
all remaining versions will upload (unless there are none left, in which
case it will abort the entire upload).
