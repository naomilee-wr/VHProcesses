:orphan:
|
|
|

=========================================== 
Style Guide for Developers
===========================================

|

**Purpose**
------------------ 

This document provides information on a short list of common style issues we see in developer-written documentation. The full style guide for writers is available `here <http://internal.wrs.com/engineering/engops/techpubs/internal-docs/House%20Style%20Guide%208.2/index.html>`__.

|

**Capitalization in Titles and Headings**
------------------------------------------------

Use mixed uppercase and lowercase for the titles in all headings at all levels. Mixed case is easier to read than all uppercase.

Capitalization follows standard practices:

- Capitalize the first and last word of the title.
- Capitalize all other words except the following:

  - articles (*the, a, an*)

  - prepositions (*about, into, since, with, and so forth*) except those with more than five letters (for example, between should be capitalized)

  - conjunctions fewer than five letters (*and, but, for, or, nor*)

  - the words *to* and *as*

- Capitalize literal names--such as commands, libraries, and routines--exactly, no matter what position they occupy in the heading; their capitalization must never be altered.
- Capitalize each element of a hyphenated word as if it were a separate word, except when the element is not the first word and would normally not be capitalized:

  - articles (*the, a, an*)

  - prepositions (*about, into, since, with, and so forth*) except those with more than five letters (for example, between should be capitalized)

  - conjunctions fewer than five letters (*and, but, for, or, nor*)

  - the words *to* and *as*

This capitalization standard applies to all headings, including topic and section titles, figure and table headings, and column headings in tables. However, it does not apply to steps.

Example:  Capitalizing First, Last, and Intermediate Words

- An Overview of Workbench
- Programming with VxWorks
- About Semaphores
- Distinguishing between Nouns and Verbs

Example:  Capitalizing Literals

- Using the foo( ) Routine
- The WIND_BASE Environment Variable

Example:  Capitalizing Hyphenated Words

- Attach-to-Target
- Cross-Development
- On-Chip
- Plug-in
- Pop-up
- Real-Time
- Run-Time
- Third-Party

|
 
**Command-Line Prompts**
-----------------------------

For command-line example displays, use the standard system prompts.

The standard system prompts are as follows:

*%*

For UNIX shell commands.

*$*

For Linux shell commands.

*#*

For UNIX and Linux shell commands that must be executed as root/superuser.

*C:\>*

For Windows commands.

*->*

For standard VxWorks and host shell prompts.

|
 
**Contractions**
---------------------

Do not use contractions; for example, don't, doesn't, can't, it's.

Contractions are informal and are often misunderstood by non-native English speakers.

|
 
**Defining Acronyms**
---------------------------

All acronyms should be defined at first usage, except for widely recognized acronyms such as those included in the table below. At first usage, the full definition should be given, followed by the acronym in parentheses; 

*for example:*

- Internet Control Message Protocol (ICMP)
- board support Package (BSP)
- real-time process (RTP)

If the first usage of an acronym appears in a heading, do not define it in the heading; rather, define it in the text that follows the heading.

In topic-based writing, the first usage in a topic must be defined. In chapter-based writing, it is acceptable to define it the first time it is used in a book or chapter.

When giving the full definition, do not artificially capitalize letters in mid-word to indicate how the acronym was derived. In particular, note that definitions for many acronyms should not be capitalized at all (for example, *fd*, for file descriptor). In general, acronyms that stand for proper nouns should be capitalized, while those that stand for regular nouns should not be.

|

**Common Acronyms (Do not define)**
------------------------------------

+--------------------------------+--------------------------------------------------------+
|         **Acronym**            |                **Definition**                          |
+--------------------------------+--------------------------------------------------------+
|ASCII                           |	American Standard Code for Information Interchange|
+--------------------------------+--------------------------------------------------------+
|ANSI                            |	American National Standards Institute             |
+--------------------------------+--------------------------------------------------------+
|API                             |  application programming interface                     |
+--------------------------------+--------------------------------------------------------+
|CPU                             |	central processing unit                           |
+--------------------------------+--------------------------------------------------------+
|DOS                             |	Disk Operating System                             |
+--------------------------------+--------------------------------------------------------+
|EOF                             |	end-of-file                                       |
+--------------------------------+--------------------------------------------------------+
|FCC                             |  Federal Communications Commission                     |
+--------------------------------+--------------------------------------------------------+
|FTP                             |	File Transfer Protocol                            |
+--------------------------------+--------------------------------------------------------+
|GUI                             |	graphical user interface                          |
+--------------------------------+--------------------------------------------------------+
|IEEE                            |	Institute of Electrical and Electronics Engineers |
+--------------------------------+--------------------------------------------------------+
|I/O                             |	input/output                                      |
+--------------------------------+--------------------------------------------------------+
|IP                              |	Internet Protocol                                 |
+--------------------------------+--------------------------------------------------------+
|LAN                             |	local-area network                                |
+--------------------------------+--------------------------------------------------------+
|NFS                             |	Network File System                               |
+--------------------------------+--------------------------------------------------------+
|PDF                             |	Portable Document Format                          |
+--------------------------------+--------------------------------------------------------+
|PPP                             |	Point-to-Point Protocol                           |
+--------------------------------+--------------------------------------------------------+
|PTY                             |	pseudo terminal device                            |
+--------------------------------+--------------------------------------------------------+
|RAM                             |	random access memory                              |
+--------------------------------+--------------------------------------------------------+
|ROM                             |	read-only memory                                  |
+--------------------------------+--------------------------------------------------------+
|RSH                             |	Remote Shell                                      |
+--------------------------------+--------------------------------------------------------+
|TCP                             |	Transmission Control Protocol                     |
+--------------------------------+--------------------------------------------------------+
|TFTP                            |	Trivial File Transfer Protocol                    |
+--------------------------------+--------------------------------------------------------+
|TTY                             |	teletypewriter (terminal device)                  |
+--------------------------------+--------------------------------------------------------+
|URL                             |	Uniform Resource Locator                          |
+--------------------------------+--------------------------------------------------------+
|WAN                             |	wide-area network                                 |
+--------------------------------+--------------------------------------------------------+

|

**Excluded Articles**
---------------------

Do not use abbreviated English by excluding articles (*the, a, an*).

Always use articles as required by standard English usage.

However, there is one major exception: reference-entry title lines (under NAME) may be too long to fit comfortably on a single line, particularly when the function or library name is long. This may cause the title to wrap in the table of contents. In such cases, abbreviating by excluding articles is an acceptable and necessary practice.

|

**Latin Words and Phrases**
---------------------------

Do not use Latin words and abbreviations. Choose English-language alternatives.

The following substitutes are useful:

*etc.*

and so on, and so forth, among others

*e.g.*

for example, such as

*i.e.*

that is

*via*

through, by way of, using, with

One reason for this rule is that readers commonly confuse the distinction between *e.g.* and *i.e.*

Note that *for example* and *that is* should precede, not follow, the phrase to which they refer and should generally be preceded by a semicolon. They should also be followed by a comma or colon. For example: This parameter must be a power of 2; that is: 1, 2, 4, 8, and so on.

Avoid constructions that use and so on (and its relatives) unless necessary. Lists preceded with such as are often a reasonable alternative. Never conclude a such as list with and so on (or its relatives).

|

**Present Tense**
--------------------

Assume that your reader is doing the actions you describe while reading your document.

- Use present tense wherever possible.

  INCORRECT:

  If there is not enough memory, the routine will return ERROR.

  If..., you will need to configure your own PPP framework.

  CORRECT:

  If there is not enough memory, the routine returns ERROR.

  If..., you must configure your own PPP framework.

- Avoid past and future tenses unless they are essential to convey the idea.

  CORRECT:

  If you already performed this task, continue with the next task in the workflow.

  WPA is an interim standard that will be replaced with the IEEE 802.11i standard when 802.11i is complete.
  
|
 
**Problem Words**
------------------

Certain words are often misused in technical writing. Wind River has standards for how they should be used.

 
*and/or*

Do not use. Whether "or" is exclusive or inclusive is nearly always evident from context.

 

*like/as*

Use like to compare objects or ideas. Use as to show similarity in actions.

INCORRECT:  Winston tastes good like a cigarette should.

Although the form of this colloquialism is widely used, avoid it in formal English.

 

*that/which*

The words that and which are not interchangeable. They change the meaning of a sentence depending on how you use them.

- If you want to restrict the sentence to refer to a specific case, you can use that with no comma.

  I will shop at a Safeway that is open 24 hours.

  In this example, you are saying that you are only willing to shop at a 24-hour Safeway. This case is called a restrictive or defining clause.

- If you want to provide information only, use which with a comma.

  I will shop at a Safeway, which is open 24 hours.

  In this example, you are saying that you are willing to shop at any Safeway and Safeways can be presumed to be open 24 hours. This case is called a non-restrictive or parenthetical clause.

A useful rule-of-thumb is:

- Use which with a comma when you could substitute parentheses without changing the meaning of the sentence.
- Use that with no comma when substituting parentheses would change the meaning of the sentence by remove a restriction.
 
 

*data*

Treat the word data as singular. Historically, this word has been considered plural, but is now well established as either a singular and plural noun

 

*however*

Do not position the word however in the middle of a clause (an interruption) or at the end of a clause (too late to offer much value). However is a powerful word for clarifying contrast; making it the first word in a contrasting clause is the best way to prompt the reader that what you are about to do is show the other side of the coin.

 

*it*

When the word it requires no antecedent it is known as an indefinite it. Avoid starting sentences with an indefinite it that adds nothing to the meaning; 

for example:

- It will be seen that...

- It is the purpose of...

- It is important to consider that...

Avoid using an indefinite it along with other instances of it that do require antecedents, in the same paragraph as well as the same sentence:

- It is up to the user to know how this could affect it.

 

*please*

Do not use the word please when instructing users to do something.

 

*recommend*

INCORRECT:

- We recommend...

- It is recommended...

CORRECT:

- Wind River recommends...

 

*should*

Avoid using the word should in ways the suggest equivocation or lack of firmness. Do not is considerably stronger than should not. For example:

- WEAK:

  The -nostdinc flag should not be used with the current release since it prevents the compilers from finding headers such as stddef.h.

- STRONG:

  Do not use the -nostdinc flag with the current release. It prevents...

In cases where a should sentence cannot be reworded in the imperative, the word must is a stronger choice than should.

 

*so*

Do not introduce a clause with the word so (without that). Doing so is a colloquialism. Even though its meaning in conversation may be made clear by inflection, in print it can be ambiguous. 

In the example, no close( ) function has been specified, so no driver functions are called.

Does the writer mean therefore no driver functions are called or so that no driver functions are called? The comma suggests the former, but explicitly using thus, therefore, or so that would have left no doubt as to the intended meaning.

 

*supported/unsupported*

To say that a feature or function is supported is to say that it is part of Wind River's product or service and that Customer Support is available. The converse is true for *unsupported*: it is not part of our product or service and Customer Support is not available.

Do not use *unsupported* to mean that something does not work; in such cases, be direct about the fact that it does not work.

 

*use*

Do not overuse the word use. Look for alternative words, such as with, or verbs that are more descriptive. For example, a function can be called instead of used.

 

*user*

Do not write user in place of you; do not speak of the reader in the third person.

INCORRECT:

- The user should...

CORRECT:

- You must...
 
 

*we/our*

Do not use first-person pronouns, even the impersonal we. For example:

INCORRECT:

- As we have seen in the examples above...

- Our online support site provides...

- We recommend...

- Contact us for...

CORRECT:

- As illustrated in the examples above...

- Wind River Online Support provides...

- Wind River recommends...

- Contact Wind River...

- Contact your sales representative...

 

*wish*

Do not use the word wish; use want instead.

 

*you, your*

Addressing examples to the reader by writing you and your is acceptable; in fact, in distinctly tutorial documentation, these words are desirable. However, apply them sparingly and do not overuse. While judicious use of you/your can engage the reader, excessive or unnecessary use can easily become a distraction.

Avoid using a you construction when a simple imperative statement does the job more succinctly. For example, instead of "you configure the facility by...", write "Configure the facility by..."

|
  
**Product Names**
-------------------

Always use the full and properly capitalized product name. For example, always use VxWorks, not vxworks or Vxworks.

 
**Proper Adjectives**
----------------------

A proper adjective is an adjective that is derived from a proper name. In the following example, **main()** is a proper adjective:

- Use the main() function to ...

In sentences that contain proper adjectives, the proper adjective should always come before the noun.

CORRECT:    
     
- Use the main function() to ...

INCORRECT:
       
- Use the function main() to ...

 
**Spelling and Special Terms**
--------------------------------------

Wind River uses the following spelling conventions for common terms in our documentation. For items not on this list, use the `Merriam-Webster dictionary <https://www.merriam-webster.com>`__.

+-------------------------------------------+---------------------------------------------------+
|                **USE..**                  |                    **NOT..**                      |
+-------------------------------------------+---------------------------------------------------+
| and so forth, among others	            | etc.                                              |
+-------------------------------------------+---------------------------------------------------+
| autoscaling	                            | auto scaling, auto-scaling                        |
+-------------------------------------------+---------------------------------------------------+
| back end	                            | backend                                           |
+-------------------------------------------+---------------------------------------------------+
| back up (verb)	                    | backup, back-up                                   |
+-------------------------------------------+---------------------------------------------------+
| backup (n., adj.)	                    | back up, back-up                                  |
+-------------------------------------------+---------------------------------------------------+
| backward	                            | backwards                                         |
+-------------------------------------------+---------------------------------------------------+
| baseline	                            | base line                                         |
+-------------------------------------------+---------------------------------------------------+
| basename (of filename)	            | base name                                         |
+-------------------------------------------+---------------------------------------------------+
| bit-field	                            | bit field                                         |
+-------------------------------------------+---------------------------------------------------+
| boot line	                            | bootline, boot-line                               |
+-------------------------------------------+---------------------------------------------------+
| boot loader                               | bootloader                                        |
+-------------------------------------------+---------------------------------------------------+
| boot ROM                                  | bootrom, boot rom, bootROM                        |
+-------------------------------------------+---------------------------------------------------+
| bps	                                    | BPS, baud                                         |
+-------------------------------------------+---------------------------------------------------+
| bring up (v.)                             | bringup, bring-up                                 |
+-------------------------------------------+---------------------------------------------------+
| bring-up (n., adj.)	                    | bringup, bring up                                 |
+-------------------------------------------+---------------------------------------------------+
| cacheable	                            | cachable                                          |
+-------------------------------------------+---------------------------------------------------+
| caching	                            | cacheing                                          |
+-------------------------------------------+---------------------------------------------------+
| callback	                            | call-back                                         |
+-------------------------------------------+---------------------------------------------------+
| cannot	                            | can not                                           |
+-------------------------------------------+---------------------------------------------------+
| CD-ROM	                            | CDROM, cdrom                                      |
+-------------------------------------------+---------------------------------------------------+
| check in (v.)                             | checkin, check-in                                 |
+-------------------------------------------+---------------------------------------------------+
| check out (v.)	                    | checkout, check-out                               |
+-------------------------------------------+---------------------------------------------------+
| checkin (n., adj.)                        | check in, check-in                                |
+-------------------------------------------+---------------------------------------------------+
| checkout (n., adj.)	                    | check out, check-out                              |
+-------------------------------------------+---------------------------------------------------+
| clean up (v.)	                            | cleanup, clean-up                                 |
+-------------------------------------------+---------------------------------------------------+
| cleanup (n., adj.)                        | clean up, clean-up                                |
+-------------------------------------------+---------------------------------------------------+
| coprocessor	                            | co-processor                                      |
+-------------------------------------------+---------------------------------------------------+
| countdown	                            | count-down                                        |
+-------------------------------------------+---------------------------------------------------+
| cross-compiler	                    | cross compiler                                    |
+-------------------------------------------+---------------------------------------------------+
| cross-development	                    | cross development                                 |
+-------------------------------------------+---------------------------------------------------+
| cross-reference                           | cross reference                                   |
+-------------------------------------------+---------------------------------------------------+
| data type	                            | datatype                                          |
+-------------------------------------------+---------------------------------------------------+
| decrypt	                            | unencrypt, de-encrypt                             |
+-------------------------------------------+---------------------------------------------------+
| dialog	                            | dialogue                                          |
+-------------------------------------------+---------------------------------------------------+
| email                                     | e-mail, E-mail                                    |
+-------------------------------------------+---------------------------------------------------+
| Ethernet	                            | ethernet                                          |
+-------------------------------------------+---------------------------------------------------+
| Excelan	                            | Excellan                                          |
+-------------------------------------------+---------------------------------------------------+
| extensible	                            | extendable, extendible                            |
+-------------------------------------------+---------------------------------------------------+
| fax	                                    | FAX                                               |
+-------------------------------------------+---------------------------------------------------+
| fd	                                    | FD                                                |
+-------------------------------------------+---------------------------------------------------+
| file name	                            | filename                                          |
+-------------------------------------------+---------------------------------------------------+
| file system	                            | filesystem                                        |
+-------------------------------------------+---------------------------------------------------+
| flash (n.)                                | Flash, flash (v.) or flashing (gerund)            |
+-------------------------------------------+---------------------------------------------------+
| floating-point	                    | floating point                                    |
+-------------------------------------------+---------------------------------------------------+
| follow up (v.)	                    | followup, follow-up                               |
+-------------------------------------------+---------------------------------------------------+
| followup (n., adj.)	                    | follow up, follow-up                              |
+-------------------------------------------+---------------------------------------------------+
| for example e.g. 	                    | e.g.                                              |
+-------------------------------------------+---------------------------------------------------+
| FTP                                       | ftp                                               |
+-------------------------------------------+---------------------------------------------------+
| hardcopy	                            | hard copy                                         |
+-------------------------------------------+---------------------------------------------------+
| home page	                            | homepage                                          |
+-------------------------------------------+---------------------------------------------------+
| hot swap	                            | hotswap                                           |
+-------------------------------------------+---------------------------------------------------+
| HP-UX	HP/UX,                              | HPUX                                              |
+-------------------------------------------+---------------------------------------------------+
| I/O	                                    | i/o, IO, io                                       |
+-------------------------------------------+---------------------------------------------------+
| ID	                                    | id                                                |
+-------------------------------------------+---------------------------------------------------+
| inline	                            | in-line                                           |
+-------------------------------------------+---------------------------------------------------+
| inter-process	                            | interprocess                                      |
+-------------------------------------------+---------------------------------------------------+
| Internet	                            | internet                                          |
+-------------------------------------------+---------------------------------------------------+
| intertask                                 | inter-task                                        |
+-------------------------------------------+---------------------------------------------------+
| ioctl()	                            | IOCTL, IOctl, IOCtl, ioctl                        |
+-------------------------------------------+---------------------------------------------------+
| Iostreams (no bold)	                    | IOStreams, iostreams, IoStreams                   |
+-------------------------------------------+---------------------------------------------------+
| KB	                                    | Kb, Kbyte                                         |
+-------------------------------------------+---------------------------------------------------+
| log in (v.)                               | login, log-in                                     |
+-------------------------------------------+---------------------------------------------------+
| log out (v.)	                            | logout, log-out                                   |
+-------------------------------------------+---------------------------------------------------+
| login (n., adj.)	                    | log in, log-in                                    |
+-------------------------------------------+---------------------------------------------------+
| logout (n., adj.)	                    | log out, log-out                                  |
+-------------------------------------------+---------------------------------------------------+
| lowercase                                 | lower-case                                        |
+-------------------------------------------+---------------------------------------------------+
| make up (v.)	                            | makeup, make-up                                   |
+-------------------------------------------+---------------------------------------------------+
| makeup (n., adj.)	                    | make up, make-up                                  |
+-------------------------------------------+---------------------------------------------------+
| MB	                                    | Mb, Mbyte                                         |
+-------------------------------------------+---------------------------------------------------+
| motherboard	                            | mother-board, mother board                        |
+-------------------------------------------+---------------------------------------------------+
| MS-DOS	                            | MSDOS, MS DOS                                     |
+-------------------------------------------+---------------------------------------------------+ 
| multi-core	                            | multicore, Multicore                              |
+-------------------------------------------+---------------------------------------------------+
| multi-user                                | multiuser                                         |
+-------------------------------------------+---------------------------------------------------+
| multi-WAN, Multi-WAN	                    | multiwan, Multiwan, multiWAN                      |
+-------------------------------------------+---------------------------------------------------+
| multiprocessor                            | multi-processor                                   |
+-------------------------------------------+---------------------------------------------------+
| multitasking	                            | multi-tasking                                     |
+-------------------------------------------+---------------------------------------------------+
| mux	                                    | MUX                                               |
+-------------------------------------------+---------------------------------------------------+
| nonvolatile	                            | non-volatile                                      |
+-------------------------------------------+---------------------------------------------------+
| nonzero	                            | non-zero                                          |
+-------------------------------------------+---------------------------------------------------+
| offload	                            | off-load                                          |
+-------------------------------------------+---------------------------------------------------+
| on-board	                            | on board, onboard                                 |
+-------------------------------------------+---------------------------------------------------+
| online	                            | on-line                                           |
+-------------------------------------------+---------------------------------------------------+
| overrun	                            | over-run, over run                                |
+-------------------------------------------+---------------------------------------------------+
| overwrite                                 | over-write, over write                            |
+-------------------------------------------+---------------------------------------------------+
| PAL                                       | pal                                               |
+-------------------------------------------+---------------------------------------------------+
| pathname	                            | path name                                         |
+-------------------------------------------+---------------------------------------------------+
| Platform product	                    | platform product                                  |
+-------------------------------------------+---------------------------------------------------+
| plug-in	                            | plugin                                            |
+-------------------------------------------+---------------------------------------------------+
| pop-up	                            | popup                                             |
+-------------------------------------------+---------------------------------------------------+
| POSIX	                                    | Posix                                             |
+-------------------------------------------+---------------------------------------------------+
| power up (v.)	                            | powerup, power-up                                 |
+-------------------------------------------+---------------------------------------------------+
| powerup (n., adj.)	                    | power up, power-up                                |
+-------------------------------------------+---------------------------------------------------+
| preemptive	                            | pre-emptive                                       |
+-------------------------------------------+---------------------------------------------------+
| print out (v.)	                    | printout, print-out                               |
+-------------------------------------------+---------------------------------------------------+
| printout (n., adj.)	                    | print out, print-out                              |
+-------------------------------------------+---------------------------------------------------+
| real-time, Real-Time	                    | realtime, Real-time                               |
+-------------------------------------------+---------------------------------------------------+
| reentrant	                            | re-entrant                                        |
+-------------------------------------------+---------------------------------------------------+
| ROMFS                                     | romfs (unless a literal)                          |
+-------------------------------------------+---------------------------------------------------+
| RSH	                                    | rsh                                               |
+-------------------------------------------+---------------------------------------------------+
| run time (n.)	                            | runtime, run-time                                 |
+-------------------------------------------+---------------------------------------------------+
| run-time (adj.)                           | runtime, run time                                 |
+-------------------------------------------+---------------------------------------------------+
| SBus	                                    | S-Bus, Sbus                                       |
+-------------------------------------------+---------------------------------------------------+
| scalable	                            | scaleable                                         |
+-------------------------------------------+---------------------------------------------------+
| SCSI                                      | Scsi, scsi                                        |
+-------------------------------------------+---------------------------------------------------+
| set up (v.)	                            | set-up                                            |
+-------------------------------------------+---------------------------------------------------+
| setup (n., adj.)	                    | set-up                                            |
+-------------------------------------------+---------------------------------------------------+
| shell script	                            | shellscript                                       |
+-------------------------------------------+---------------------------------------------------+
| shut down (v.)	                    | shutdown, shut-down                               |
+-------------------------------------------+---------------------------------------------------+
| shutdown (n., adj.)	                    | shut down, shut-down                              |
+-------------------------------------------+---------------------------------------------------+
| single-stepping	                    | single stepping                                   |
+-------------------------------------------+---------------------------------------------------+
| spinlock	                            | spin-lock                                         |
+-------------------------------------------+---------------------------------------------------+
| standalone	                            | stand-alone                                       |
+-------------------------------------------+---------------------------------------------------+
| start up (v.)	                            | startup, start-up                                 |
+-------------------------------------------+---------------------------------------------------+
| startup (n., adj.)	                    | start-up                                          |
+-------------------------------------------+---------------------------------------------------+
| stdio.h	                            | stdio                                             |
+-------------------------------------------+---------------------------------------------------+
| subclass                                  | sub-class                                         |
+-------------------------------------------+---------------------------------------------------+
| subdirectory	                            | sub-directory                                     |
+-------------------------------------------+---------------------------------------------------+
| SunOS	                                    | SUN OS                                            |
+-------------------------------------------+---------------------------------------------------+
| superclass	                            | super-class                                       |
+-------------------------------------------+---------------------------------------------------+
| task ID	                            | task id                                           |
+-------------------------------------------+---------------------------------------------------+
| Tcl	                                    | TCL, tcl                                          |
+-------------------------------------------+---------------------------------------------------+
| TFTP	                                    | tftp                                              |
+-------------------------------------------+---------------------------------------------------+
| that is	                            | i.e.                                              |
+-------------------------------------------+---------------------------------------------------+
| timeout	                            | time-out                                          |
+-------------------------------------------+---------------------------------------------------+
| timestamp	                            | time stamp, time-stamp                            |
+-------------------------------------------+---------------------------------------------------+ 
| title bar	                            | titlebar                                          |
+-------------------------------------------+---------------------------------------------------+ 
| TTY	                                    | tty                                               |
+-------------------------------------------+---------------------------------------------------+
| turn off (v.)                             | turnoff, turn-off                                 | 
+-------------------------------------------+---------------------------------------------------+
| turnoff (n., adj.)                        | turn off, turn-off                                |
+-------------------------------------------+---------------------------------------------------+
| underrun	                            | under-run, under run                              |
+-------------------------------------------+---------------------------------------------------+
| UNIX	                                    | Unix                                              |
+-------------------------------------------+---------------------------------------------------+
| uppercase	                            | upper-case, upper case                            |
+-------------------------------------------+---------------------------------------------------+
| user space                                | userspace                                         |
+-------------------------------------------+---------------------------------------------------+
| Users' Group	                            | User's Group, Users Group                         |
+-------------------------------------------+---------------------------------------------------+
| VxWorks	                            | VxWORKS, VXWORKS, vxWorks                         |
+-------------------------------------------+---------------------------------------------------+
| Web                                       | web                                               |
+-------------------------------------------+---------------------------------------------------+
| website                                   | Web site, web site                                |
+-------------------------------------------+---------------------------------------------------+
| Wind River                                | WindRiver, Wind River Systems, Inc.               |
+-------------------------------------------+---------------------------------------------------+
| work around (v.)	                    | workaround, work-around                           |
+-------------------------------------------+---------------------------------------------------+
| workaround (n., adj.)	                    | work around, work-around                          |
+-------------------------------------------+---------------------------------------------------+
| write-through, write-back	            | writethrough, writeback                           |
+-------------------------------------------+---------------------------------------------------+

|

**Special Terms**
---------------------

Always define special terms when they are introduced if there is any doubt as to whether they are generally accepted or understood.

 
The following terms are used variously in our industry, or in some cases are a source of confusion:

*API*

The term API (application programming interface) refers to a collection of functions. Do not use it to mean a single function or call. It is incorrect to say "The doorClose( ) API closes the door." Instead, say "The doorClose( ) function closes the door."

*argument*

See parameter.

*argument list*

The set of arguments that is given to a command or routine when it is executed. Compare parameter list.

*baud, baud rate*

Strictly speaking, baud is a rate, which means that baud rate is redundant. However, baud rate is common parlance and used widely, and we have interface parameters with names like baudrate; therefore, the term baud rate is acceptable.

*decrypt*

See encrypt.

*deprecated*

A feature that has been deprecated is still supported in the current release, but its use is discouraged and it will not be supported in future releases. Declaring that a feature has been deprecated serves as a warning to customers that they should seek an alternative solution. Do not be specific about when or in what release support for a deprecated feature will be discontinued.

Note that it is not correct to say that a feature will be deprecated in the future, because future discontinuance is built into the definition of deprecate. Use the present perfect and say a feature has been deprecated. Do not say a feature is deprecated.

*disc*

Use only to refer to a CD or DVD, not a hard disk.

*disk*

Use only to refer to a hard disk or floppy disk, not a CD or DVD.

*encrypt*

Do not use unencrypt to mean the opposite of encrypt; use decrypt instead. However, it is acceptable to say something is unencrypted, but that should only mean that something is simply not in an encrypted state, rather than actively deciphered or decoded.

*endianness*

This is a legitimate term that refers to the byte order characteristic of specific processors--big-endian and little-endian.

*function*

For C language, use the term function rather than routine. This is a change to previous usage.

Do not use this word to indicate the purpose of some software component or to describe how something operates. For this purpose, use functionality or capability.

*function pointer*

Continue to use the term function pointer. This is the most commonly understood term for this element, and it also corresponds with the FUNCPTR data type and other similarly named data types.

*interpreter*

See shell.

*interrupt service routine, ISR, interrupt handler*

Although these terms are synonymous, use interrupt service routine and ISR for consistency.

*operating systems*

When possible, spell out this term. When you must abbreviate, use OSs.

*parameter*

The terms parameter and argument are similar. However, argument is more narrowly used to refer either to command-line options passed to a command or to the values or options that may be given to a function when it is called. The term parameter is used not only to refer to arguments but more broadly to refer to options that may be set in any number of ways, as, for example, in a configuration file.

*parameter list*

The set of possible parameters or argument types that may be given to a command or routine when it is executed. Compare argument list.

*release*

Use release to indicate the numbered iteration of a product. In other words, "VxWorks 6.2" refers to release 6.2. 

Use version to refer to other variants of a product, such as host or architecture, but do not use version to indicate a release. Use version also to refer to host or target variants of a book.

Although these words are often used synonymously in the industry, the term release more narrowly reflects the notion of the product's level of revision as it is made publicly available, while version is more loosely used to mean not only release, but variation by host, target, architecture, and other differentiating factors.

Note that other departments at Wind River are not always consistent and occasionally use version to mean release.

*routine*

See function.

*run-time, run time*

Do not use the word *run-time* as a noun meaning *run-time component*. The word is an adjective, as in run-time environment, run-time version, and run-time activity. The term run time (with a space) is a noun meaning the time period in which a program runs or the amount of time needed to run a program (in contrast to compile time.)

*shell*

A shell is the command-line interface for human interaction with a system. An interpreter is the software that converts what the user enters into action. An interpreter is similar to a compiler, except that the compiler works on files and the interpreter works on individual commands or on scripts containing individual commands.

VxWorks provides a shell that runs on the host and a kernel shell that runs on the target device. UNIX and Linux provide shells. Each shell provides a default interpreter (for example, csh or Bash) but may support other interpreters as well.

Correct:

- Use this set of commands with the C interpreter and that set of commands with the Tcl interpreter.
- Switch from the Tcl interpreter to the C interpreter by entering "C" at the shell prompt.
- There are several standard shells available in Linux: sh, bash, dash, csh. Other shells are available as well, but not as popular.
- Type exit and a carriage return to exit the C interpreter and return to the shell.

Incorrect:

- command interpreter shell
- command shell interpreter
- shell interpreter
- "Type the ls command to the interpreter.

*unencrypted*

See encrypt.

*USB flash drive*

Always use USB flash drive when referring to a USB data storage device with flash memory. Do not use the terms "stick" or "thumb-drive".

A USB flash drive should not be confused with Live USB. Live USB is a USB flash drive or hard disk drive that contains an operating system and can be booted. It may also be used for product installation.

*version*

See discussion of release, above.

| 
 
**Voice**
----------

Use active voice whenever possible.

Active voice specifies who or what is performing the action in a sentence. It is often easier to understand and more concise than passive voice.

Using active voice also describes our software more explicitly—you explicitly identify the software thing (for example, a routine, a semaphore, a tool, or a build system) that triggers a result, providing additional detail about how our software works.

INCORRECT

- The EXAMPLE_COMP component must be added to the VIP.
- If there is not enough memory, an error is returned.

CORRECT

- Add the EXAMPLE_COMP component to the VIP.  (“You” is the implied subject that must add the component.)
- If there is not enough memory, the routine returns an error.


Only use passive voice if the person or thing performing the action is unknown or unimportant.
  
|


**Change Log**
--------------
+----------------+----------------+----------------+----------------+---------------------------------------+
| **Date**       | **Change       | **Version**    | **Change By**  | **Description**                       |
|                | Request ID**   |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 06/24/2020     | N/A            | 0.1            | Shree Vidya    | Transferred content from Style Guide  |
|                |                |                | Jayaraman      | for Developers Jive page              |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
