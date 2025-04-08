# CBT1052
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. GitHub repos will be deleted and created during this period...

```
//***FILE1052 is from Sam Golob and contains several programs       *   FILE1052
//*           that perform a unique function of being able to       *   FILE1052
//*           adjust the attributes (PRIVATE, PUBLIC, STORAGE)      *   FILE1052
//*           of mounted DASD volumes.  These are all TSO           *   FILE1052
//*           commands.                                             *   FILE1052
//*                                                                 *   FILE1052
//*           email:  sbgolob@cbttape.org                           *   FILE1052
//*                                                                 *   FILE1052
//*           These programs use the UCB Lookup Table (ULUT)        *   FILE1052
//*           to obtain REAL UCB's, which are then zapped           *   FILE1052
//*           accordingly.  Therefore they work only on fairly      *   FILE1052
//*           recent levels of MVS (since ESA 5.2.2 approximately)  *   FILE1052
//*                                                                 *   FILE1052
//*           These programs can be used (in a pinch) to replace    *   FILE1052
//*           the function of the console MOUNT commands:           *   FILE1052
//*                                                                 *   FILE1052
//*           MOUNT uuuu,VOL=(SL,volser),USE=PRIVATE                *   FILE1052
//*                                          PUBLIC                 *   FILE1052
//*                                          STORAGE                *   FILE1052
//*                                                                 *   FILE1052
//*           In addition, two other programs are provided:         *   FILE1052
//*                                                                 *   FILE1052
//*           DVAT     - Tells you the incore status of the         *   FILE1052
//*                      VATLSTxx PARMLIB settings.  These          *   FILE1052
//*                      settings do not change until the           *   FILE1052
//*                      next IPL, so you can use them for          *   FILE1052
//*                      reference, as to how to adjust the         *   FILE1052
//*                      attributes of your DASD volumes.           *   FILE1052
//*                                                                 *   FILE1052
//*           UCBPRIA  - A TSO command to convert all online        *   FILE1052
//*                      DASD to USE=PRIVATE (which should be       *   FILE1052
//*                      followed by MOUNT console commands,        *   FILE1052
//*                      or UCBSTOR or UCBPUBL commands, to         *   FILE1052
//*                      create STORAGE DASD packs, or PUBLIC       *   FILE1052
//*                      DASD packs).  You NEED at least one        *   FILE1052
//*                      STORAGE pack on your system, and           *   FILE1052
//*                      preferably more of then.                   *   FILE1052
//*                                                                 *   FILE1052
//*           Other programs:                                       *   FILE1052
//*                                                                 *   FILE1052
//*           UCBSTOR  - Set the attributes of a volume to          *   FILE1052
//*                      STORAGE                                    *   FILE1052
//*                                                                 *   FILE1052
//*           UCBPUBL  - Set the attributes of a volume to          *   FILE1052
//*                      PUBLIC                                     *   FILE1052
//*                                                                 *   FILE1052
//*           UCBPRIV  - Set the attributes of a volume to          *   FILE1052
//*                      PRIVATE                                    *   FILE1052
//*                                                                 *   FILE1052
//*           All programs except DVAT have to be APF-authorized    *   FILE1052
//*           because they zap the real UCB's.  Also, the UCBDASD   *   FILE1052
//*           TSO command, which displays REAL UCB's (not copies)   *   FILE1052
//*           DOES NOT have to be APF-authorized.                   *   FILE1052
//*                                                                 *   FILE1052
//*           Additionally, to help you view large output which     *   FILE1052
//*           is PUTLINE'd, the four REXX execs from Mark Zelden    *   FILE1052
//*           called TSOE, TSOV, TSOB, and TSOR are included in     *   FILE1052
//*           this file for your convenience.  To use these execs   *   FILE1052
//*           you say (for example):                                *   FILE1052
//*                                                                 *   FILE1052
//*           TSO TSOV tsocmd parms   (to VIEW the command output)  *   FILE1052
//*               TSOE                    EDIT                      *   FILE1052
//*               TSOB                    REVIEW                    *   FILE1052
//*               TSOR                    BROWSE                    *   FILE1052
//*                                                                 *   FILE1052
//*           To further help you assess the attributes of your     *   FILE1052
//*           online disk packs, we have included the unauthorized  *   FILE1052
//*           program UCBDASD (which happens to be the precursor    *   FILE1052
//*           of most of the new programs included here).           *   FILE1052
//*                                                                 *   FILE1052
```
