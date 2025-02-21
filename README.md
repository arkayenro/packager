## Building for multiple game clients

This fork is designed to handle multiple and/or client specific TOC files.

- Retail
  - AddOnName_Mainline.toc
  - AddOnName-Mainline.toc
  - AddOnName.toc

- Cataclysm
  - AddOnName_Cata.toc
  - AddOnName-Cata.toc
  - AddOnName.toc

- Wrath
  - AddOnName_Wrath.toc
  - AddOnName-Wrath.toc
  - AddOnName.toc

- BCC
  - AddOnName_TBC.toc
  - AddOnName_BCC.toc
  - AddOnName-TBC.toc
  - AddOnName-BCC.toc
  - AddOnName.toc

- Classic Era
  - AddOnName_Vanilla.toc
  - AddOnName_Classic.toc
  - AddOnName-Vanilla.toc
  - AddOnName-Classic.toc
  - AddOnName.toc


While you do not require an AddOnName.toc for the game to work, if you remove that and only have the AddOnName-ClientType.toc
variants some hosting services cannot handle that situation (eg CurseForge will reject the upload for not having a TOC file) so you
may be better off leaving it as the default "global" format.

Use of the -g option should not be required, and is untested so i have no idea
what it will do, so dont use it.

All you need to do is setup toc files for the clients that your addon supports (with
the appropriate interface versions in them) and a single zip file will be built, uploaded,
and tagged for each of the interface versions that the hosting site supports.

note - some of the hosting sites do not support all interface versions.
Where they do not support a specific interface version you have set then that
version will be removed from the upload and you will receive a warning,
all remaining versions will upload (unless there are none left, in which
case it will abort the entire upload).
