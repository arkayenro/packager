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

Use of the -g option is untested and probably wont work.


All you need to do is setup the client specific toc files your addon supports (with
the appropriate interface values in them) and a single file will be upploaded and
tagged for each game version that the hosting site accepts.

note - some of the hosting sites do not support all interface versions.
Where they do not support a specific toc version you have set then that
version will be removed from the upload and you will receive an error,
all remaining versions will upload (unless there are none left, in which
case it will abort the entire upload).
