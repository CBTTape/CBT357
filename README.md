# CBT357
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 357 This file contains several utilities to process       *   FILE 357
//*           partitioned data sets, some COBOL and PL/I            *   FILE 357
//*           utilities, and a number of ISPF EDIT and DS List      *   FILE 357
//*           macros. All are freeware to be used as desired.       *   FILE 357
//*           The utilities are now all in an unloaded member,      *   FILE 357
//*           @LOADLIB.                                             *   FILE 357
//*                                                                 *   FILE 357
//*               C_Hafner@HotMail.Com                              *   FILE 357
//*                                                                 *   FILE 357
//*       File Contents:                                            *   FILE 357
//*                                                                 *   FILE 357
//*       $$$NOTE  -- Introductory release notes                    *   FILE 357
//*       @FILE357 -- Simple description of file content  (this     *   FILE 357
//*                   file)                                         *   FILE 357
//*       @MACDOC# -- Documentation for all Edit & CLIST macros     *   FILE 357
//*                   expamded with carriage control                *   FILE 357
//*       @MACDOCO -- Documentation for all Edit & CLIST macros     *   FILE 357
//*       @PGMDOC# -- Documentation for the included programs       *   FILE 357
//*       @PGMDOCO -- Documentation for the included programs       *   FILE 357
//*                   expanded with carriage control                *   FILE 357
//*                                                                 *   FILE 357
//*       ABENDX   -- Abend with supplied user or system code       *   FILE 357
//*       ABENDX$  -- Sample JCL for ABENDX                         *   FILE 357
//*       ADDCC    -- Revise sequential file into printable file    *   FILE 357
//*                   using script tags                             *   FILE 357
//*       ADDCC$   -- Sample JCL for ADDCC                          *   FILE 357
//*       ADDCC@   -- Add carriage control to any sequential file   *   FILE 357
//*       ADDCOLS  -- Add columns (from Mark Zelden) of different   *   FILE 357
//*                   types                                         *   FILE 357
//*       ADDFLAG  -- Add revision flags to selected lines          *   FILE 357
//*       ADDLINEA -- Part of ADDLINES                              *   FILE 357
//*       ADDLINEB -- Part of ADDLINES                              *   FILE 357
//*       ADDLINES -- Add a member before or after every other      *   FILE 357
//*                   member in a PDS                               *   FILE 357
//*       ALIGN    -- Align code based on a string                  *   FILE 357
//*       ALIGNALL -- Align data based on delimiters                *   FILE 357
//*       ALIGNAX  -- Align data based on delimiters and removing   *   FILE 357
//*                   them                                          *   FILE 357
//*       ALIGNS   -- Align code based on a string with             *   FILE 357
//*                   minimal spaces utilized                       *   FILE 357
//*       ALLMEM   -- Execute a macro against every member of a     *   FILE 357
//*                   PDS (see ALLMEMC and ALLMEMF)                 *   FILE 357
//*       ALLMEMC  -- Sample change macro for ALLMEM                *   FILE 357
//*       ALLMEMF  -- Sample find macro for ALLMEM                  *   FILE 357
//*       ALLOC    -- Dynamic allocation macro                      *   FILE 357
//*       ALLOCGDX -- Allocate a relative GDG as an absolute one    *   FILE 357
//*       ALPHACNT -- COBOL alphanumeric count routines             *   FILE 357
//*       ASAXWC   -- IBM wildcard macro                            *   FILE 357
//*       ASAXWC$  -- Sample use of ASAXWC                          *   FILE 357
//*       BASEASM  -- Basic assembler read and write program        *   FILE 357
//*       BASECOB  -- Basic COBOL read and write program            *   FILE 357
//*       BASEEZ   -- Basic Easytrieve read and write program       *   FILE 357
//*       BASEPLI  -- Basic PL/I read and write program             *   FILE 357
//*       BC       -- Blank selected columns                        *   FILE 357
//*       BLDLR    -- Routine to get member directory data          *   FILE 357
//*       BNCHMKA  -- Assembler benchmark skeleton                  *   FILE 357
//*       BNCHMKC  -- COBOL benchmark skeleton                      *   FILE 357
//*       BNCHMKP  -- PL/I benchmark skeleton                       *   FILE 357
//*       BS       -- Optimal block size calculator                 *   FILE 357
//*       CC       -- Simple calculator                             *   FILE 357
//*       CENTER   -- Center text                                   *   FILE 357
//*       CHDEL    -- Dynamically create HDELs for files to be      *   FILE 357
//*                   deleted                                       *   FILE 357
//*       CLONE    -- Create a copy of a data set under ISPF DSList *   FILE 357
//*       CLONER   -- Create a copy of a data set under ISPF DSList *   FILE 357
//*                   and replace an existing data set              *   FILE 357
//*       CLRSCRN  -- Routine to clear TSO screen                   *   FILE 357
//*       CLS      -- Macro to invoke CLRSCRN to clear TSO screen   *   FILE 357
//*       CLS2REXX -- Macro to convert CLIST to REXX EXEC           *   FILE 357
//*       COBBITS  -- COBOL bit manipulation sub-programs           *   FILE 357
//*       COBCOLOF -- Put COBOL structure offsets into columns 73   *   FILE 357
//*                   thru 80 using FileAid                         *   FILE 357
//*       COBCOLOI -- Put COBOL structure offsets into columns 73   *   FILE 357
//*                   thru 80 using InSync                          *   FILE 357
//*       COBCOLSF -- Put COBOL structure offsets into columns 73   *   FILE 357
//*                   thru 80 using FileAid                         *   FILE 357
//*       COBCOLSI -- Put COBOL structure offsets into columns 73   *   FILE 357
//*                   thru 80 using InSync                          *   FILE 357
//*       COBCOLVF -- View FileAid layout of COBOL structure        *   FILE 357
//*       COBCOLVI -- View InSync layout of COBOL structure         *   FILE 357
//*       COBCPUTM -- Sample COBOL CPU calculation code from MVS    *   FILE 357
//*                   Help site                                     *   FILE 357
//*       COBHEXR  -- COBOL hex conversion sub-program              *   FILE 357
//*       COBLKLST -- COBOL LE link list sample                     *   FILE 357
//*       COL      -- Macro to insert column string                 *   FILE 357
//*       COLS     -- Macro to insert column string                 *   FILE 357
//*       COLSCC   -- Macro to insert column string over range      *   FILE 357
//*                   from Jim Haire                                *   FILE 357
//*       COMPRS   -- Macro to compress PDS from within Edit        *   FILE 357
//*       CONBLANK -- Consolidate 2 or more blank lines to one      *   FILE 357
//*       CONCATDD -- Concatenate a data set to a DD                *   FILE 357
//*       COPYCOLS -- Copy column data                              *   FILE 357
//*       COPYINS  -- Copy and insert column data                   *   FILE 357
//*       COUNTX   -- Show record count from DS List (ISPF 3.4)     *   FILE 357
//*                   for sequential or VSAM files                  *   FILE 357
//*       COUNTXNX -- Count excluded and included lines             *   FILE 357
//*       CU       -- Insert IEFBR14 data set clean up JCL          *   FILE 357
//*       CUD      -- Dynamically insert data set clean up JCL      *   FILE 357
//*       CUTX     -- Tweaked cut type macro                        *   FILE 357
//*       CVB      -- Convert display numeric to binary             *   FILE 357
//*       CVD      -- Convert binary to display numeric             *   FILE 357
//*       C2H      -- Convert characters to hex equivalent          *   FILE 357
//*       DELBLANK -- Delete blank lines                            *   FILE 357
//*       DELCOLS  -- Delete column data                            *   FILE 357
//*       DELDUPS  -- Sort file and delete duplicate lines          *   FILE 357
//*       DELDUPX  -- Delete contiguous duplicate lines             *   FILE 357
//*       DELPARA  -- Delete debug lines from DISPARA & DISPVAR     *   FILE 357
//*       DESC     -- Macro to show LRECL, BLKSIZE and count        *   FILE 357
//*       DETAB    -- Restructure tabbed file                       *   FILE 357
//*       DETAB$   -- JCL for DETAB                                 *   FILE 357
//*       DIRLIST  -- Hex list of a directory separating each member*   FILE 357
//*       DIRLIST$ -- JCL for DIRLIST                               *   FILE 357
//*       DIRSCNC  -- COBOL directory generator                     *   FILE 357
//*       DIRSCNC$ -- JCL for DIRSCNC                               *   FILE 357
//*       DIRSCNQ  -- PL/I directort generator                      *   FILE 357
//*       DIRSCNQ$ -- JCL for DIRSCNQ                               *   FILE 357
//*       DISPARA  -- Add DISPLAY at start of every paragraph       *   FILE 357
//*       DISPDSN  -- Reverse DSN=...,DISP=SHR to DISP=SHR,DSN=...  *   FILE 357
//*       DISPVAR  -- Add DISPLAY line for variable under cursor    *   FILE 357
//*       DYNA     -- Sample dynamic allocator using MACSDYNA       *   FILE 357
//*       DYNAMC   -- Sample COBOL dynamic allocation using BPXWDYN *   FILE 357
//*       DYNAMP   -- Sample PL/I dynamic allocation using BPXWDYN  *   FILE 357
//*       DYNCOB   -- Sample COBOL dynamic allocation using DYNA    *   FILE 357
//*       DYNF     -- Sample dynamic free using MACSDYNA            *   FILE 357
//*       DYNI     -- Sample dynamic internal reader using MACSDYNA *   FILE 357
//*       DYNN     -- Sample dynamic allocation using MACSDYNA      *   FILE 357
//*       DYNPLIA  -- Sample PL/I dynamic allocation using DYNA     *   FILE 357
//*       DYNPLII  -- Sample PL/I dynamic internal reader using DYNA*   FILE 357
//*       DYNPLIN  -- Sample PL/I dynamic allocation using DYNA     *   FILE 357
//*       DYNPLIS  -- Sample PL/I dynamic SYSOUT using DYNA         *   FILE 357
//*       DYNS     -- Sample dynamic SYSOUT using MACSDYNA          *   FILE 357
//*       EMPTY    -- Remove data from DS List sequential or PDS    *   FILE 357
//*       EMPTYCK$ -- Use IDCAMS to set return code indicating      *   FILE 357
//*                   whether a dataset is really empty             *   FILE 357
//*       ENC      -- Simple encryption macro                       *   FILE 357
//*       ENC2     -- Improved ENC encryption macro                 *   FILE 357
//*       EZCKGRDT -- Easytrieve Gregorian daet check               *   FILE 357
//*       EZCKJUDT -- Easytrieve Julian date check                  *   FILE 357
//*       EZCL     -- Easytrieve link sample                        *   FILE 357
//*       EZCOPY   -- Easytrieve simple copy                        *   FILE 357
//*       EZCOUNT  -- Easytrieve record count                       *   FILE 357
//*       EZGENRPT -- Easytrieve sample most options                *   FILE 357
//*       EZPARM   -- Easytrieve sample PARM usage                  *   FILE 357
//*       EZSTRSK  -- Easytrieve string search using STRSRCH macro  *   FILE 357
//*       EZUNPK   -- Easytrieve unpack sample                      *   FILE 357
//*       FALT     -- Dummy macro to allow repeat of FN, FGE, etc   *   FILE 357
//*       FAND     -- Show lines with all specified strings         *   FILE 357
//*       FEXC     -- Find the next excluded line                   *   FILE 357
//*       FGE      -- Find line with value greater then some value  *   FILE 357
//*       FGT      -- Find line with value greater then or equal    *   FILE 357
//*       FILLCOLS -- Overlay data columns with string              *   FILE 357
//*       FILLINS  -- Insert string into data columns               *   FILE 357
//*       FINDDUPS -- Sort and show duplicate lines                 *   FILE 357
//*       FINDDUPX -- Show duplicate lines                          *   FILE 357
//*       FINDNSTR -- Do SuperC in DS List for members w/o string   *   FILE 357
//*       FINDSTRX -- Do SuperC in DS List for members w/ string    *   FILE 357
//*       FLAGREVS -- Show which lines of a member changed in Edit  *   FILE 357
//*                   before saving                                 *   FILE 357
//*       FLE      -- Find line with value less then some value     *   FILE 357
//*       FLT      -- Find line with value less then or equal       *   FILE 357
//*       FMAX     -- Find largest value in some columns            *   FILE 357
//*       FMDOUBLE -- COBOL convert float to display for Easytrieve *   FILE 357
//*       FMIN     -- Find smallest value in some columns           *   FILE 357
//*       FN       -- Repeatable find of line with value not        *   FILE 357
//*       FNB      -- Find non blank values                         *   FILE 357
//*       FNOT     -- Show lines with none of given strings         *   FILE 357
//*       FOG      -- Random text generator                         *   FILE 357
//*       FOR      -- Show lines with any of the given strings      *   FILE 357
//*       FOREVER  -- Generate job to "touch" list of data sets     *   FILE 357
//*       FOREVERX -- Sample EXEC to "touch" list of data sets      *   FILE 357
//*       FORMCOLS -- Reformat arithmetic data using a format       *   FILE 357
//*       FPEND    -- Find the lines with a pending prefix command  *   FILE 357
//*       FREE     -- Dynamic allocation macro                      *   FILE 357
//*       FS       -- Submit PDS scan for string macro              *   FILE 357
//*       FX       -- Exclude all except lines with string          *   FILE 357
//*       GATHERX  -- Pull all excluded lines together              *   FILE 357
//*       GETDSN   -- Routine to get data set name from COBOL       *   FILE 357
//*       GETDSNS  -- Paste wildcard list of data sets into file    *   FILE 357
//*       GETGDGS  -- Generate GDG list or DD images                *   FILE 357
//*       GETMEMS  -- Generate selected member list after cursor    *   FILE 357
//*       GETRGNSZ -- Show TSO region size                          *   FILE 357
//*       GMT      -- Show Greenwich offset to local time           *   FILE 357
//*       HEXDUMP  -- Dump data in hex/character format as logical  *   FILE 357
//*                   records                                       *   FILE 357
//*       HEXDUMP$ -- JCL for HEXDUMP                               *   FILE 357
//*       HEXUDUM  -- Dump data in hex/character format as          *   FILE 357
//*                   unformatted records                           *   FILE 357
//*       HEXUDUM$ -- JCL for HEXUDUMP                              *   FILE 357
//*       HEXUIDC$ -- IDCAMS PRINT DUMP sample                      *   FILE 357
//*       HOWLONG  -- Show the larget and smallest record size      *   FILE 357
//*       HSMDOC   -- Quick reference to HSM commands               *   FILE 357
//*       H2C      -- Hex to character equivalent macro converter   *   FILE 357
//*       IE       -- Insert COBOL code for EVALUATE structure      *   FILE 357
//*       IEZBITS  -- IBM bit equivalence assembler macro           *   FILE 357
//*       II       -- Insert COBOL code for IF/ELSE/END-IF structure*   FILE 357
//*       IP       -- Insert COBOL code for PERFORM structure       *   FILE 357
//*       IPADDR   -- Get IP address                                *   FILE 357
//*       IS       -- Insert COBOL code for SEARCH structure        *   FILE 357
//*       ISA      -- Insert COBOL code for SEARCH ALL structure    *   FILE 357
//*       ISORT    -- Insert COBOL code for Sort JCL                *   FILE 357
//*       IST      -- Insert COBOL code for STRING structure        *   FILE 357
//*       JB       -- Jump back to PERFORM statement                *   FILE 357
//*       JC       -- Insert job card at front of file              *   FILE 357
//*       JOBINFO  -- COBOL sample grabbing job information from    *   FILE 357
//*                   control tables                                *   FILE 357
//*       JOINCOLS -- Join columns with Edit macro                  *   FILE 357
//*       JT       -- Jump to paragraph being PERFORMed             *   FILE 357
//*       KEEPCOLS -- Keep specified columns, deleting others       *   FILE 357
//*       LASTREF  -- Show the last reference date in DS List       *   FILE 357
//*       LESS     -- Exclude additional lines                      *   FILE 357
//*       LJUST    -- Left justify text                             *   FILE 357
//*       LKDT     -- Show link date                                *   FILE 357
//*       LMODWU   -- Load module where used                        *   FILE 357
//*       LMODWU$  -- JCL for LMODWU                                *   FILE 357
//*       LMODXRF  -- Load module cross reference                   *   FILE 357
//*       LMODXRF$ -- JCL for LMODXRF                               *   FILE 357
//*       LONGEST  -- Show the longest line                         *   FILE 357
//*       MACSDYNA -- Dynamic allocation macros (many)              *   FILE 357
//*       MORE     -- Unexclude additional lines                    *   FILE 357
//*       MOVECOLD -- Move column data deleting original columns    *   FILE 357
//*       MOVECOLS -- Move column data                              *   FILE 357
//*       MOVEINS  -- Move and insert column data                   *   FILE 357
//*       MOVEINSD -- Insert column data and delete original data   *   FILE 357
//*       NEATJCL  -- Format JCL                                    *   FILE 357
//*       NEW      -- Allocate a sequential file                    *   FILE 357
//*       NEWP     -- Allocate a PDS                                *   FILE 357
//*       NUMCOLS  -- Place numbers in specific columns             *   FILE 357
//*       NUMCOLS0 -- Place zero padded numbers in specific         *   FILE 357
//*       OPCODE   -- Describe instruction associated with          *   FILE 357
//*       PA       -- PASTEAFT equivalent for IBM CUT/PASTE commands*   FILE 357
//*       PACKDS   -- Compress file using IBM TRSMAIN               *   FILE 357
//*       PAGES    -- Select pages from large sequential carriage   *   FILE 357
//*       PAGES$   -- Sample JCL for PAGES                          *   FILE 357
//*       PASTEAFT -- Copy CUTX lines after one or more lines       *   FILE 357
//*       PASTEX   -- A paste variation                             *   FILE 357
//*       PASTY    -- Do PASTEX with a PF Key                       *   FILE 357
//*       PDSGEN   -- Generate data with member/data set tokens     *   FILE 357
//*       PDSGEN$  -- JCL for PDSGEN                                *   FILE 357
//*       PDSLIST  -- List concatenated PDS's of any record format  *   FILE 357
//*       PDSLIST$ -- JCL for PDSLIST                               *   FILE 357
//*       PDSMATC  -- Generate SUPERC compares for unequal PDSMATCH *   FILE 357
//*                   members                                       *   FILE 357
//*       PDSMATC$ -- JCL for PDSMATCH                              *   FILE 357
//*       PDSMATC@ -- JCL for PDSMATCH and PDSMATC                  *   FILE 357
//*       PDSMATCH -- Match 2 PDS's by name, statistics or data     *   FILE 357
//*                   (Updated to fix a bug. False equal if more    *   FILE 357
//*                    data was in the second file. - 12/2015)      *   FILE 357
//*                   (Second bug. Null members compared not equal) *   FILE 357
//*                   (Fix to do multiple GETMAINs that will        *   FILE 357
//*                    accommodate a directory of any size.)        *   FILE 357
//*                   (Fix to solve RECFM=VB problem.)              *   FILE 357
//*       PDSPUNC$ -- JCL for PDSPUNCH                              *   FILE 357
//*       PDSPUNCH -- Make an IEBUPDTE ADD/REPL file of             *   FILE 357
//*       PDS2SEQ  -- Put PDS members into sequential file          *   FILE 357
//*       PK       -- Pack numbers (into COMP-3 format)             *   FILE 357
//*       PULL     -- Select 1 or more sets of records from any     *   FILE 357
//*       PULL$    -- Sample JCL for PULL                           *   FILE 357
//*       PY       -- Equivalent of PASTY for IBM CUT/PASTE         *   FILE 357
//*       QCLONE   -- Submit of CLONE equivalent job                *   FILE 357
//*       QCLONER  -- Submit of CLONER equivalent job               *   FILE 357
//*       RANCOLS  -- Generate random numbers into specific         *   FILE 357
//*       RANCOLS0 -- Generate zero padded random numbers into      *   FILE 357
//*       REALUNIQ -- Find only really unique lines with sort       *   FILE 357
//*       REALUNIX -- Find only really unique lines with out sort   *   FILE 357
//*       REGS     -- Assembler register naming generator           *   FILE 357
//*       RENTER   -- Assembler reenterable prologue macro          *   FILE 357
//*       REVERSEX -- Reverse line order                            *   FILE 357
//*       REXIT    -- Assembler reenterable exit macro              *   FILE 357
//*       RJUST    -- Right justify text                            *   FILE 357
//*       SAVEINPL -- Save edited member in place                   *   FILE 357
//*       SCANPDS  -- Simple SuperC example                         *   FILE 357
//*       SCANPDSX -- SuperC with options shown                     *   FILE 357
//*       SETRC    -- Set return code for MVS COND checking         *   FILE 357
//*       SETRC$   -- Sample JCL for SETRC                          *   FILE 357
//*       SHIFT    -- Shift columns                                 *   FILE 357
//*       SHORTEST -- Find shortest line                            *   FILE 357
//*       SHUFFLE  -- Randomize line order                          *   FILE 357
//*       SLEEP    -- Pause for # seconds                           *   FILE 357
//*       SMARTGN  -- Generate control cards from list              *   FILE 357
//*       SMARTGN$ -- Sample JCL for SMARTGN                        *   FILE 357
//*       SNACK    -- Exclude all but lines w/ variable under       *   FILE 357
//*                   cursor                                        *   FILE 357
//*       SORTNX   -- Sort non excluded lines keeping the excluded  *   FILE 357
//*       SORTX    -- Documented sample sort controls               *   FILE 357
//*       SPLITAFT -- Split selected lines after given string       *   FILE 357
//*       SPLITON  -- Split selected lines at given string          *   FILE 357
//*       SPLTCOLS -- Split one line into several                   *   FILE 357
//*       SQUSH    -- Eliminate multiple blanks                     *   FILE 357
//*       STEMSRT1 -- REXX stem sort via quick sort w/ timings      *   FILE 357
//*       STEMSRT2 -- REXX stem sort via shell sort w/ timings      *   FILE 357
//*       STEMSRT3 -- REXX stem sort via call to sort w/ timings    *   FILE 357
//*       STOWR    -- Save member directory information routine     *   FILE 357
//*       STOWU    -- Null member directory information routine     *   FILE 357
//*       STRING   -- Gilbert's assembler DISPLAY macro             *   FILE 357
//*       STRING$  -- Sample JCL using STRING                       *   FILE 357
//*       STRING#  -- Documentation for STRING                      *   FILE 357
//*       STRSRCH  -- Easytrieve string search macro                *   FILE 357
//*       STRSRCH# -- Documentation for STRSRCH                     *   FILE 357
//*       STRUCT   -- Show program structure (COBOL, EZTrieve,      *   FILE 357
//*       SUBCAN   -- Submit job and cancel edit session            *   FILE 357
//*       SUBO     -- Submit job with substituted variables with    *   FILE 357
//*                   ORIGIN as default                             *   FILE 357
//*       SUBX     -- Submit job with substituted variables         *   FILE 357
//*       SUFFLINE -- Add suffix to selected lines                  *   FILE 357
//*       SUMCOLS  -- Sum columns                                   *   FILE 357
//*       SYSI     -- Show some TSO parameters                      *   FILE 357
//*       TD       -- Remove directory statistics                   *   FILE 357
//*       TERSE$   -- IBM compression sample                        *   FILE 357
//*       TODAY    -- Show variations of a given date               *   FILE 357
//*       TOUCH    -- Change any ISPF statistics from batch         *   FILE 357
//*       TOUCH$   -- JCL for TOUCH                                 *   FILE 357
//*       TRAP     -- Macro to trap output of TSO command           *   FILE 357
//*       TSJ      -- Do text split and join via PF Key             *   FILE 357
//*       TU       -- Update directory statistics                   *   FILE 357
//*       T1       -- Start macro timing                            *   FILE 357
//*       T2       -- Stop and display macro timing                 *   FILE 357
//*       UNIQUE   -- Sort and show unique lines                    *   FILE 357
//*       UNIQUEX  -- Show unique lines                             *   FILE 357
//*       UNPACKDS -- Decompress file using IBM TRSMAIN             *   FILE 357
//*       UNPK     -- Turn packed data into displayable data        *   FILE 357
//*       UNTOUCH  -- Eliminate any ISPF statistics from batch      *   FILE 357
//*       UNTOUCH$ -- JCL for UNTOUCH                               *   FILE 357
//*       VALUES   -- Summarize actual content of 1 or more sets of *   FILE 357
//*       VALUES$  -- JCL for VALUES                                *   FILE 357
//*       VERASE   -- Reset CUTX lines in Profile                   *   FILE 357
//*       VSAVE    -- Save file under View                          *   FILE 357
//*       VW       -- View file                                     *   FILE 357
//*       VWV      -- Gather and View part of VSAM file             *   FILE 357
//*       WAIT     -- Batch sleep routine                           *   FILE 357
//*       WAIT$    -- Gather and View part of VSAM file             *   FILE 357
//*       XALLMEM  -- Execute EXEC against another PDS              *   FILE 357
//*       XCOPY    -- Copy outside data source from command line    *   FILE 357
//*       XINDENT  -- Exclude to line with same indentation         *   FILE 357
//*       ZVW      -- View file under cursor                        *   FILE 357
//*                                                                 *   FILE 357
```
