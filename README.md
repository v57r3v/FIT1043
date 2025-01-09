java c
FIT1043 Assignment 3: Specification 
Due date:   Friday   18th October 2024 -   11:55   pm
Aim Assignment   1      2   walked   you   through   what   you   have   learnt   in   Lectures   1   to   7 and   also the Collection, Wrangling, Analyse and Present phases of our Standard   Value   Chain. It   provides   you   an   introduction   to   the   data   science   lifecycle. This   assignment   is   related   to   the   latter   part   of   this   unit,   where   we   used   BASH   shell   and   R   programming   language   to   work   with   large   datasets.   It   will test your ability   to:
● Read a   reasonably   large dataset,
●       Process the dataset   using   BASH   Shell   Scripts,
●       Conduct aggregation of the   dataset   content,
● Read data from a   file   in   R,   and
●       Generate appropriate visualisations in   R and   output   to   files.
Data 
The   dataset   for   this   assignment   is   available   on   Moodle.   It   is   a   compressed   file   that   contains   pre-processed   twitter   content   sourced   from   Sentiment140 Dataset on   Kaggle.   The   original   source   contained   1.6   million tweets, extracted using the   Twitter API   and   they   have   been   labelled   as   negative   (0),   neutral   (2),   or positive   (4). The data on   Moodle for this assignment is a   subset   of   the   original   dataset. The columns are the same,   and   are   as follows:
●       target: the polarity of the tweet (e.g.,   0   =   negative,   2   =   neutral,   4   =   positive)
● ids: The   id of the tweet   (e.g., 2087)
●       date: the date of the tweet (e.g.,   Sat   May   16   23:58:44   UTC   2009)
●       flag: The query. If there   is   no query, then this   value   is   NO_QUERY.
●          user: the user that tweeted (e.g.,   robotickilldozr)
● text: the text of the tweet   (e.g.,   Lyx   is cool)
Note:   You   will   need   to   use   either   a   Linux   machine,   a   Mac   terminal   or   Cygwin   on   a   Windows   machine for this purpose.
For those who are   more curious, the   paper describing the dataset   is as follows:
●       Go,    A.,    Bhayani,    R.,        Huang, L.   (2009).   Twitter   sentiment   classification
using distant supervision. CS224N   project   report, Stanford,   1(12), 2009.
Hand-in Requirements 
Please   hand   in a single   PDF file only and a video   file   (refer   to Task B). PDF file should consist of: 
1.    Answers   to   the   questions.    In   order   to   justify   your   answers   to   all   the   questions,   make sure   to
a.      Include   screenshots/images   of   the   graphs   or   outputs   you   generate   (You   will need to   use screen-capture functionality to create appropriate   images.)
b.      Explain what each   part of the command does for all your answers.
For   instance,   if   the   code   you   use   is   ‘unzip   tutorial_data.zip‘,   you   need   to   explain that the code   is used to   uncompress the   zip   file.
c.      Copy   and   paste   your   Unix   code   from   Bash   Shell and the   R code (Do Not include screenshots of your code).
d.      Kindly Do    Not copy    the    questions,    else    you    might      have    high    Turnitin
similarity due to all submissions referring to the   same   set   of questions.
Assignment Tasks: In   this   assignment   you   will   work   with   a   large   data   set   (in this case, just   more than a   million   lines   of data)   and   will   use   shell   scripts to   process and aggregate   data.   In the   whole   exercise,   you   must   NOT   uncompress   the   data   and   store   it.   Once   the   data   is   aggregated    and    properly    formatted,    you   will   then    read   the   data    in    R   to   conduct   further    analysis.    In this assignment you will only use R   to read   some   data   and   provide visualisations for the latter tasks.
Note,   for   this   assignment   you   are   required   to   write shell commands to   answer   all   questions   in Task A   unless the   instructions specify   using R code.
Task A: Download    the   file    FIT1043_Dataset.gz   from   Moodle.    Use   the   BASH   shell   to   manipulate   the   file   and   answer   the   following   questions.   Show   the   BASH   shell   command you used and also the displayed output where   appropriate.
A1. Inspecting the data (3 marks) 
1.      State   the   size   (in   Bytes   or   MegaBytes)   of the   FIT1043_Dataset.gz   file   and   provide the shell command that you used to   determine   the   size.
2.    What    delimiter      is      used    to    separate    the      columns      in    the    file?      Do   illustrate   how you deduced this.
3.      How   many   lines   are   there   in   the   dataset?   Again,   provide   a   single   line code on   how you   obtained   it.
A2. Information from Data (5 marks) 
1.      How   many   unique   users   are   there   in   the dataset?   Provide a single   line of code   that   uses   the   “awk”   and   “uniq”   commands.   You   are   also   req代 写FIT1043 Assignment 3: SpecificationR
代做程序编程语言uired   to   read   the “man” pages   of the   “uniq”   command   to   figure   out   if it   is sufficient to answer the   question.   Explain   the   code   you   provided.
2.    What   is   the   date   range   for   the   Twitter   posts   in   this   file?   (Assume   that   the   data   is ordered   by date   in chronological   order)
3.      For   each   of the   sub-questions   below,   provide a single   line code (one   each)   and briefly   explain your   code.
a.      How       many       tweets       mentioned         the       word       “France”       in       any   combination of uppercase or lowercase   letters   .
b.      How   many   of   those   are   not   spelt   exactly   “france”   or   “France”   but   in   other    combinations    of    uppercase      and      lowercase      (e.g.,      FRance    or   francE).
c.      Output   the   lines   of A2.3 (b) into   a   file   called   myText.txt   (not   the   number of lines but   the specific   lines that   are   returned).
A3. Data aggregation (4.5 marks) 
1.      Find    the      total       number    of       negative,      neutral,      and      positive    tweets      that   mentioned   the   word   “USA”   (ignore   case).   Then   find   the   total   number   of   negative,   neutral,   and   positive   tweets   that   mentioned   the word      “Canada”   (ignore   case).
2.      Store    the      data    from    A3.1      in      files      named       sentiment-USA.csv   and   sentiment-canada.csv respectively,   using   the   following output format   (Note,   you   can   manually   create   the   csv   files   using   output   numbers   from   the shell commands):
Negative,   99   Neutral,   99      Positive,   99
3. [R Code] Use   the   files   sentiment-USA.csv and   sentiment-canada.csv   from A3.2 and   read   both files   using   R.
4. [R code] Using   the   data   from   both   countries,   plot   two   separate   bar   charts:   one   for   the   USA   and   one   for   Canada.   Then   copy   the   bar   charts   and   paste   them   in   your   PDF   report.   You   will   get   a   bonus   mark   if you   plot   a side   by side   bar chart   instead of two separate bar   charts.
5.      In   your   report, analyse and discuss the differences observed   between the two   bar charts, considering aspects such as overall sentiment   distribution.
A4. Small Challenge (3.5 marks) 
Let’s   assume   that   we   want   to   consider   tweets   that   contain   the   word   “Australia”   from   the data   provided.
1.      To   answer   this   question,   you   will   need   to   first   extract   the   timestamps   of   the   tweets    (date    column)    referring    to    “Australia”      (ignore      case)      using    the      BASH   Shell, and save the timestamps   into a file   named aus_time.txt.
2. [R    code] You   will   then    need   to    read   aus_time.txt    in    R.    Note   that    R   will    not   recognise   the   strings   as   timestamps   automatically,   and   for   this   task   you   are   to   convert   them   from   text   values   using   the   strptime()function.   Instructions   on   how   to    use    the    function    are   availablehere.   You   will   need   to   write   a   format string,   e.g.,   starting   with   “   %a   %b”   to   tell   the   function   how to   parse the   particular   date/time format   in your file.   Explain this   in your answer.
3. [R code] Using   the   data   processed   in   A4.1   and   A4.2,   calculate   the   number   of   tweets   for   each   day.   After   performing   this   aggregation,   create   a   histogram   to   visualise    the    daily      tweet      counts.      Discuss      the      distribution      of      tweets      in      your   histogram,   noting any patterns you observe.
Task B: Video Preparation (4 marks) Presentation   is   one   of   the   important   steps   in   a   data   science   process.   In   this   task   you   will   need   to   prepare   an up to 3 minutes video of yourself (you can share your   code   on   screen) and describe your approach on the above task   (Task A4).
●       Please make sure to   keep your camera   on   (show   yourself)   during   recording.
Clarifications Do    use    the      Ed      Forum    so      that      other      students      can      participate      and      contribute.      For   postings    on    the    forum,    do    use   it   as   though   you   are   asking   others   (instead   of   your   lecturer   or   tutors   only)   for   their   opinions   or   interpretation.   Just   note   that   you   are   not   to   post answers directly.
Congratulations! You   have completed all   FIT1043 assignments and you will   have only the   final   exam   left.   I   do   hope   that   you   have   been   well   introduced   to   the   world   of   Data   Science,   which   still   requires    significant    effort    and    there    is    lots    more    to    learn.    Hopefully   those   skills   will   contribute to your lifelong   learning!




         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
