# gpl-history

This is a collection of historical variants of various GPL and LGPL license
texts as published by the FSF and GNU project as well as key adopters (such
as the Linux kernel and GNU Bash, GCC or Findutils).

It started as a tongue-in-cheek exercise after some exchanges with Linus,
Alan Cox and other kernel maintainers on LKML while I was working as an Elf
helper to Thomas Gleixner during the 2017-2019 campaign to clean up the kernel
licensing documentation. There was an argument about which source to use for the
GPL text and whether the text used in Linux was correct, and I jumped in with
some GPL text history.

This repo is an attempt to store it all in git.

Why? The GPL starts with this:

    Everyone is permitted to copy and distribute verbatim copies
    of this license document, but changing it is not allowed.

If you take this statement literally, "verbatim" becomes slightly more flexible
if there are more textual variants to chose from, which happens to be the case.

Note also that any attempt to use strict checksums to identify a license is
a weak approach since there are so many small variants.

The `COPYING` and `linux.COPYING` files have a partially reconstructed and
incomplete git history.

The `allvers` directory contains every known version without any attempt to craft
a proper git history; instead each version is a new file and there is a .notes
files with notes and URLs.

There are also branches that contained the filtered Linux commit/patches history
for the Linux `COPYING` file (built using historical Linux trees and lengthy git
filter-branch), but this is incomplete.

---------

Big thanks to:
 - Armijn Hemel @armijnhemel for helping maintaining this and reporting several
   new variants

---------

On 2017-12-28 COPYING file from the Linux kernel moves to LICENSES/preferred/GPL-2.0

The Linux COPYING's history ends and meets and collides with this COPYING and
GPL history! As a weird twist of fate the efforts of licensing clarification in
the Linux kernel that led to the creation of this history as a tongu-in-cheek
also altered the history of the Linux kernel COPYING file itself. This is the
problem with time-travel: if you travel back in time, you will alter history
and create a new now and a possibly different future.

For the history of history, here is the full commit message from Thomas Gleixner
forever binding this repository history to Linux commit history:

---------

    LICENSES: Add the GPL 2.0 license
    Add the full text of the GPL 2.0 license to the LICENSES directory.  It was
    copied directly from the COPYING file in the kernel source tree as it
    differs from the public available version of the license in various places
    including the FSF.
    
    Philippe did some research on the GPL2.0 history:
    
      There is NO trustworthy version of an official GPL 2.0 text: the FSF
      official texts are all fubar (if only in small and subtle ways). The FSF
      texts should be authoritative, but then which one? They published more
      GPL 2.0 versions than most. So we would be hard pressed to blame SPDX or
      the OSI for having their own minor variant.
    
      Then in digging further, I found the ONE true original GPL with a file
      time stamp on June 2 1991, 01:50 (AM?, PM? unknown time zone?)  ! in an
      old GCC archive.
    
      For the posterity and everyone's enjoyment I have built a git history
      of GPL 2.0 Mark1 to Mark6
    
      See https://github.com/pombredanne/gpl-history/commits/master/COPYING
    
      I also added a shorter history of the Linux COPYING text. The first
      version in Linus's git tree is based on the very fine and well tuned GPL
      2 Mark4, the first fully Y2K compliant version of the GPL 2, as you can
      see from the diffs with the former Mark3: that was dangerously stuck in
      the last century.
    
      The current version in is based on a rare GPL 2.0 Mark5.1 aka "Franklin
      St", that I do not have in my history yet and spells "Franklin St."
      rather than "Franklin Street."  Therefore there is likely another GPL 2.0
      version between Mark4 and Mark5 that I have yet to find and may not have
      been caught by the archive.org spiders. Here help and patches welcomed:
      this is likely an important missing link.
    
      Further information about this archaelogical research;
    
      http://lkml.kernel.org/r/CAOFm3uEzRMf261+O-Nm+9HDoEn9RbFjH=5J9i1C2GgMUg2G4LA@mail.gmail.com
    
    Add the required tags for reference and tooling.
    
    Signed-off-by: Thomas Gleixner <tglx@linutronix.de>
    Reviewed-by: Greg Kroah-Hartman <gregkh@linuxfoundation.org>
    Reviewed-by: Philippe Ombredanne <pombredanne@nexb.com>
    Reviewed-by: Jonas Oberg <jonas@fsfe.org>
    Reviewed-by: Darrick J. Wong <darrick.wong@oracle.com>
    Signed-off-by: Jonathan Corbet <corbet@lwn.net>

---------





For reference: https://lkml.org/lkml/2017/11/21/261

    From    Philippe Ombredanne <>
    Date    Tue, 21 Nov 2017 14:57:05 +0100
    Subject Re: [patch V2 02/11] LICENSES: Add the GPL 2.0 license
        
    
    Alan, Linus,
    
    On Mon, Nov 20, 2017 at 4:31 PM, Alan Cox <gnomes@lxorguk.ukuu.org.uk> wrote:
    > On Sat, 18 Nov 2017 11:14:00 -0800
    > Linus Torvalds <torvalds@linux-foundation.org> wrote:
    >
    >> You may be confusing things because of a newer version.
    >>
    >> On Sat, Nov 18, 2017 at 11:03 AM, Charlemagne Lasse
    >> <charlemagnelasse@gmail.com> wrote:
    >> >
    >> > That should be "GNU Lesser General Public" and not "GNU Library General Public"
    >>
    >> That's just FSF revisionism.
    
    Linus:
    
    Revisionism it is indeed! Please see the fun and twisted tale of the
    five official GPL texts below.
    
    
    >> It used to be called "Library" over "Lesser", in the original GPL2.
    >>
    >> I suspect your other issues are similar "there's been different
    >> versions over time" things. the address being one of them.
    >>
    >> We've actually taken some of the FSF updates over the years ("19yy" ->
    >> "<year>", and the address change) but the main COPYING file still
    >> calls the LGPL the "GNU Library General Public License".
    >>
    >> I refuse to change the original copyright wording due to idiotic
    >> internal FSF politics that tried to change history.
    >
    > Do we have any files which had the later LGPL text attached to them - if
    > so then they should be keeping that header.
    >
    > Which raises another question. If there are multiple GPL 2.0 texts which
    > are *supposedly* legally identical but this has never been tested in law
    > -that implies SPDX is wrong in tagging them identically in case they turn
    > out not to be...
    
    Alan:
    
    This last comment rings as a red herring to me. There are many minute
    variations of the GPL around and these are unlikely relevant.
    No sane judge would consider any of these variations material IMHO and
    should fine and throw in jail for contempt anyone arguing that this is
    important.
    
    Now, on the fun side, I discovered a while back through fixing a bug
    in scancode-toolkit that there are FIVE versions of the official GPL
    2.0 texts published by the FSF over the years. I am ashamed that I end
    up doing this research and I would never thought I would need to
    rummage through this pile.... but that came up while reviewing kernel
    license scans and a few other scans to support Thomas and Greg
    licensing clarification efforts.
    
    Shocking, isn't it?
    
    Let me call these GPL versions the GPL-2.0.0, GPL-2.0.1, GPL-2.0.2,
    GPL-2.0.3 and GPL-2.0.4 :D
    
    (but please this one time only!, let's forget about these afterwards)
    
    GPL-2.0.4 v5. The most recent one was published after the GPL 3.0
    publication [1] [2]. It refers to the `Franklin Street` address and to
    the `GNU Lesser General Public License` top and bottom
    
    GPL-2.0.3 v4. Slightly after the HTML publication of the new address
    in v3, the address was changed in the text version [3]: It refers to
    the  `Franklin Street` address and to the `GNU Library General Public
    License` top and bottom.
    
    GPL-2.0.2 v3. The previous one in force before the publication of the
    GPL 3.0 came about the time of the FSF office move on May 1, 2005 to
    Franklin Street [4] In this HTML version, it refers to the `Franklin
    St` address and uses the `GNU Library General Public License` at the
    top and `GNU Lesser General Public License`  at the bottom with a
    conflicted opinion on which one of the LGPL 2 or 2.1 version to use.
    
    GPL-2.0.1 v2. Around December 2003, a variation was published [5]. It
    also predates the move to Franklin and it refers to the `Temple Place`
    address and the `GNU Library General Public License` at the top and
    `GNU Lesser General Public License`  at the bottom. Still split on
    confused about which LGPL version to recommend.
    
    GPL-2.0.1 v1. The one true and only original GPL 2.0.... the oldest
    cached version [6] predates the move and it refers to the `Temple
    Place` address and the `GNU Library General Public License`
    throughout.
    
    FWIW, I made sure I have all these texts as scancode detection rules
    so I would get 100% exact hash matches on these oddities.
    
    Now you will surely agree with me that the sole sane conclusion of
    studying this mess is that there must some unhappy ghost that
    triggered these text changes when the FSF moved from Temple Place to
    Franklin Street in protest for the move. The only other possible
    explanation I could fathom would be a bug in their teletype [7].
    
    [1] https://www.gnu.org/licenses/old-licenses/gpl-2.0.txt
    [2] http://web.archive.org/web/20070716031727/http://www.gnu.org/licenses/old-licenses/gpl-2.0.txt
    [3] http://web.archive.org/web/20050511030123/http://www.fsf.org/licensing/licenses/gpl.txt
    [4] http://web.archive.org/web/20050507090312/http://www.fsf.org/licensing/licenses/gpl.html
    [5] http://web.archive.org/web/20031202220858/http://www.fsf.org/copyleft/gpl.html
    [6] http://web.archive.org/web/19980119061851/http://www.fsf.org/copyleft/gpl.html
    [7] https://en.wikipedia.org/wiki/IBM_Selectric_typewriter
    -- 
    Cordially
    Philippe Ombredanne


And then https://lkml.org/lkml/2017/11/21/506 :

    From    Philippe Ombredanne <>
    Date    Tue, 21 Nov 2017 18:55:49 +0100
    Subject Re: [patch V2 02/11] LICENSES: Add the GPL 2.0 license
        
    
    On Tue, Nov 21, 2017 at 2:57 PM, Philippe Ombredanne
    <pombredanne@nexb.com> wrote:
    > Alan, Linus,
    >
    > On Mon, Nov 20, 2017 at 4:31 PM, Alan Cox <gnomes@lxorguk.ukuu.org.uk> wrote:
    >> On Sat, 18 Nov 2017 11:14:00 -0800
    >> Linus Torvalds <torvalds@linux-foundation.org> wrote:
    >>
    >>> You may be confusing things because of a newer version.
    >>>
    >>> On Sat, Nov 18, 2017 at 11:03 AM, Charlemagne Lasse
    >>> <charlemagnelasse@gmail.com> wrote:
    >>> >
    >>> > That should be "GNU Lesser General Public" and not "GNU Library General Public"
    >>>
    >>> That's just FSF revisionism.
    >
    > Linus:
    >
    > Revisionism it is indeed! Please see the fun and twisted tale of the
    > five official GPL texts below.
    >
    >
    >>> It used to be called "Library" over "Lesser", in the original GPL2.
    >>>
    >>> I suspect your other issues are similar "there's been different
    >>> versions over time" things. the address being one of them.
    >>>
    >>> We've actually taken some of the FSF updates over the years ("19yy" ->
    >>> "<year>", and the address change) but the main COPYING file still
    >>> calls the LGPL the "GNU Library General Public License".
    >>>
    >>> I refuse to change the original copyright wording due to idiotic
    >>> internal FSF politics that tried to change history.
    >>
    >> Do we have any files which had the later LGPL text attached to them - if
    >> so then they should be keeping that header.
    >>
    >> Which raises another question. If there are multiple GPL 2.0 texts which
    >> are *supposedly* legally identical but this has never been tested in law
    >> -that implies SPDX is wrong in tagging them identically in case they turn
    >> out not to be...
    >
    > Alan:
    >
    > This last comment rings as a red herring to me. There are many minute
    > variations of the GPL around and these are unlikely relevant.
    > No sane judge would consider any of these variations material IMHO and
    > should fine and throw in jail for contempt anyone arguing that this is
    > important.
    >
    > Now, on the fun side, I discovered a while back through fixing a bug
    > in scancode-toolkit that there are FIVE versions of the official GPL
    > 2.0 texts published by the FSF over the years. I am ashamed that I end
    > up doing this research and I would never thought I would need to
    > rummage through this pile.... but that came up while reviewing kernel
    > license scans and a few other scans to support Thomas and Greg
    > licensing clarification efforts.
    >
    > Shocking, isn't it?
    >
    > Let me call these GPL versions the GPL-2.0.0, GPL-2.0.1, GPL-2.0.2,
    > GPL-2.0.3 and GPL-2.0.4 :D
    >
    > (but please this one time only!, let's forget about these afterwards)
    >
    > GPL-2.0.4 v5. The most recent one was published after the GPL 3.0
    > publication [1] [2]. It refers to the `Franklin Street` address and to
    > the `GNU Lesser General Public License` top and bottom
    >
    > GPL-2.0.3 v4. Slightly after the HTML publication of the new address
    > in v3, the address was changed in the text version [3]: It refers to
    > the  `Franklin Street` address and to the `GNU Library General Public
    > License` top and bottom.
    >
    > GPL-2.0.2 v3. The previous one in force before the publication of the
    > GPL 3.0 came about the time of the FSF office move on May 1, 2005 to
    > Franklin Street [4] In this HTML version, it refers to the `Franklin
    > St` address and uses the `GNU Library General Public License` at the
    > top and `GNU Lesser General Public License`  at the bottom with a
    > conflicted opinion on which one of the LGPL 2 or 2.1 version to use.
    >
    > GPL-2.0.1 v2. Around December 2003, a variation was published [5]. It
    > also predates the move to Franklin and it refers to the `Temple Place`
    > address and the `GNU Library General Public License` at the top and
    > `GNU Lesser General Public License`  at the bottom. Still split on
    > confused about which LGPL version to recommend.
    >
    > GPL-2.0.1 v1. The one true and only original GPL 2.0.... the oldest
    > cached version [6] predates the move and it refers to the `Temple
    > Place` address and the `GNU Library General Public License`
    > throughout.
    >
    > FWIW, I made sure I have all these texts as scancode detection rules
    > so I would get 100% exact hash matches on these oddities.
    >
    > Now you will surely agree with me that the sole sane conclusion of
    > studying this mess is that there must some unhappy ghost that
    > triggered these text changes when the FSF moved from Temple Place to
    > Franklin Street in protest for the move. The only other possible
    > explanation I could fathom would be a bug in their teletype [7].
    >
    > [1] https://www.gnu.org/licenses/old-licenses/gpl-2.0.txt
    > [2] http://web.archive.org/web/20070716031727/http://www.gnu.org/licenses/old-licenses/gpl-2.0.txt
    > [3] http://web.archive.org/web/20050511030123/http://www.fsf.org/licensing/licenses/gpl.txt
    > [4] http://web.archive.org/web/20050507090312/http://www.fsf.org/licensing/licenses/gpl.html
    > [5] http://web.archive.org/web/20031202220858/http://www.fsf.org/copyleft/gpl.html
    > [6] http://web.archive.org/web/19980119061851/http://www.fsf.org/copyleft/gpl.html
    > [7] https://en.wikipedia.org/wiki/IBM_Selectric_typewriter
    
    Now in earnest here is the situation: There is NO trustworthy version
    of an official GPL 2.0 text: the FSF official texts are all fubar (if
    only in small and subtle ways). The FSF texts should be authoritative,
    but then which one? they published more GPL 2.0 versions than most. So
    we would be hard pressed to blame SPDX or the OSI for having their own
    minor variant.
    
    Then in digging further, I found the ONE true original GPL with a file
    time stamp on June 2 1991, 01:50 (AM?, PM? unknown time zone?)  ! in
    an old GCC archive.
    
    For the posterity and everyone's enjoyment I have built a git history
    of GPL 2.0 Mark1 to Mark6
    
    See https://github.com/pombredanne/gpl-history/commits/master/COPYING
    
    Each commit message has the link to the original archive.org page or
    archive download.
    
    For simplified diffs, the allvers/ dir contains all the versions of the texts.
    
    Acks and reviews are welcomed, but not really.
    
    I also added a shorter history of the Linux COPYING text. The first
    version in Linus's git tree is based on the very fine and well tuned
    GPL 2 Mark4, the first fully Y2K compliant version of the GPL 2, as
    you can see from the diffs with the former Mark3: that was dangerously
    stuck in the last century.
    
    The current version in is based on a rare GPL 2.0 Mark5.1 aka
    "Franklin St",  that I do not have in my history yet and spells
    "Franklin St." rather than "Franklin Street."
    Therefore there is likely another GPL 2.0 version between Mark4 and
    Mark5 that I have yet to find and may not have been caught by the
    archive.org spiders. Here help and patches welcomed: this is likely
    an important missing link.
    
    Linus:
    I am rather sad to see that you never adopted the GPL 2.0 Mark6 ;)
    aka. the  "final frontier" or "graveyard" release that came after the
    GPL 3 launch and when the GPL 2.0 was made an "old" license: this
    latest version is the finest ever published and I am sure we are all
    missing out something worthy!
    
    I look forward to the future publication of Mark7 and all the fine GPL
    2.0 versions to come that we should all long for.
    
    -- 
    Cordially
    Philippe Ombredanne aka. the unwelcomed GPL archeologist
