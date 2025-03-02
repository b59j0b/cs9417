java c
MATHS   7107   Data   Taming 
Assignment   1 
Trimester   1   2025 
1 Background The   Australian   Football   League   (AFL)   is   the   largest   Australian   Rules   football   league   in   the   country.    Each   week   during the season, is a new Round, where   the   teams   are   paired   up   to   play   a   match   (also   called   a   “game”).    There   are   22   rounds   in   the   season,   at   the   end   of which   the   top   eight   teams   will   compete   in   the finals matches,   culminating   in   the Grand Final where   the   premiership   cup   is   given   to   the   winner   of that   match.
There   are   two   types   of scores   in   the   game:
•   goals:   when   the   ball   goes   between   the   two   tall   posts,   worth   6   points
•   behinds:   when   the   ball   goes   between   a   tall   and   a   short   post,   worth   1   pointThe   total   score   from   the   game   for   each   team   is   given   by   adding   up   the   contributions   from   goals   and   behinds.   The total   number   of   “shots-on-goal”   is   the   number   of   goals   plus   the   number   of   behinds.    No   team   has   ever   made   more than   250   shots-on-goal   in   a   single   game.Every   team   has   a   “home”   ground,   where   they   are   based,   and   so   each   game   is   classed   as   a home game   when   they   are   playing   at   home,   or   an away game   when   they   are   not.    Currently   there   are   16   teams   in   the   league   (this scenario   is   set   in   the   past),   and   the   plan   is   that   the   league   will   not   grow   any   further,   so   the   current   list   of teams   should   not   change.   The   list   of   teams   in   the   league   is:    Adelaide,   Brisbane   Lions,   Carlton,   Collingwood,   Essendon,   Fremantle,   Geelong,   Hawthorn,   Melbourne,   North   Melbourne,   Port   Adelaide,   Richmond,   St   Kilda,   Sydney,   West   Coast   and   Western   Bulldogs.
Crowds   love   to   see   the   home   team   win.    The   company   that   sells   tickets   at   the   football   stadia   would   like   some information about whether home or away teams are   more   likely   to   win.    They also want   a   prediction   of which teams are   likely   to   play   in the   Grand   Final   (since   then   the   club’s   merchandise   is   much   more   valuable).    Coincidentally,   the   company   uses   R    and   R    Markdown,   so   they   want   your   report   as   a   PDF   generated   using   R    Markdown.    In   your   R   Markdown    code   chunks:    make   sure   that   you do not set echo    =    FALSE so   that   the   client   can   see   what   R    code   you   used   to   generate   your   output. 
1.1 Number of digits 
When writing your   own   text,   or USING the   output   from   R:
•      For   integer   results,   report   the   whole   integer.
•    For   non-integers   with   absolute   value   >   1:   use   2   decimal   places
•      For   non-integers   with   absolute   value   < 1: use 3 significant figures. For example:
◦    135.5681   ≈   135.57
◦    −0.0004586   ≈   −0.000459
If you’re just PRINTING the output   from   R, then just   keep   the   output   as   it   is.
•      Note   that   if   you   have   R    do   the   rounding   for   you   then   you   need   to   conform   to   these   two   conventions   listed   above.
2 The data 
The   company   has   four   datasets   labelled afl  * .csv (here   the   asterisk   is   a wildcard character,   meaning   it   stands   for   any   set   of characters).    Each   dataset   contains   23   columns:
• NAME:   The   team’s   name
• ROUND*:   A   description   of   the   team’s   game   in   round   “*”   .   This   column   contains   information   about:
– Won,   lost   or   drawn   status
– Home   or   away   status
– The   total   score
– The   number   of   behinds   scored
3 Data cleaning 
As   you   work   through   the   Tasks   below,   you   will   need   to   clean   the   data.
IMPORTANT! 
Make   sure   you only   remove   data   that   you   must   remove.    Do   not   just   delete   data   because it   is   convenient.   You   must   have   specific   instructions   from the   client   before you   remove   any data   from   your   analysis.
Instructions:
•    Correct   any   obvious   typos.
•    There   may   be   some   duplicated   rows,   in   which   case,   remove   one   of them.
•    Some   test   data   may   have   been   left   in.   Remove   it.
•      Any   negative   numbers   should   be   converted   to   positive   numbers.
•   If   there   are   any   values   that   are   impossible   for   some   reason   then   remove   the   entire   row.
4 Your job
Note 
Remember   that   this   is   a   report   for   a   client. 
•      Make   sure   you   write   text   to   explain   what   you   are   doing   at   each   point   and   why   you   are   doing   it.    Also   describe   the   results.    Don’t   just   state   the   R   code   that   you   are   using — the   client   can   see   that   already   —   you   need   to   describe   what   is   happening   in   a   way that   a   non-technical   person   can   understand. 
•    Don’t   include   any   unnecessary   output   or   warnings.      The   client   doesn’t   need   to   see that   and   it just   gets   in   the   way   of what   you   want   them   to   focus   on.
Closely   follow   these   steps   in   the   order   in   which   they   are   listed:
1.      Load   the   correct   dataset   as   a   tibble.   Output   all   rows   of   the   dataset.
2.   What   are   the   dimensions   of   the   data   set?
3.    Set   the   correct   seed,   then   randomly   permute   all   rows   in   your   data   set. (Hint: a random permutation is like doing a random sample of all rows.    See the Reminder Sheet.) Output   all   rows   of the   dataset.
Note 
Use this random permutation of   the data from Q3for the remainder of   the assignment (i.e. don’t   go   back   to   the   original   data   you   imported   in   Q1).
4.   We   want   to   clean   up   our   data,   but   first   we’ll   put   in   an   extra   column   of   row   numbers,   so   we   can   track   some changes   we’ve   made   to   the   data.
•    Add   a   column   at   the   far   left   of   the   dataset   called R NUM that   contains   the   row   numbers.
Output   all   rows   of the   dataset
5.      Now   we   will   clean   the   data.   Make   sure   you   justify   every   step   of   cleaning   that   you   do.
•    Remove   any   rows   that   need   removing.
•    Correct   any   errors   that   need   correcting.
•   代 写MATHS 7107 Data Taming Assignment 1 Trimester 1 2025Matlab
代做程序编程语言When   done   with   cleaning   sort   the   data   by   the   team   name.
Then   output   all   rows   of the   dataset,   and   the   dimensions   of the   data   set.
Note 
If you discover any problems with the data   in   the   following   questions   then   you   should   come   back   and   redo   this   question   before   you   submit.   Your   data   should   be   clean   and   shiny   from   this   point.
6.      Next,   let’s   tidy   the   data.
(a)    Convert   the   data   to   long   form   by   converting   the ROUND* columns   to   two   new   columns   called ROUND and OUTCOME.
(b)    Delete   the   characters   “ROUND”   from   the ROUND column   (leaving   just   the   numbers).
(c)    Using   the OUTCOME column,   create   four   new   columns:
• RESULT containing won, lost or drew 
• HOME    GAME containing TRUE or FALSE 
• TOTAL containing   the   total   score
• BEHINDS containing   the   number   of   behinds   scored
(d)    Then   delete   the OUTCOME column.
(e)    Since   we   now   have   a   larger   number   of   rows,   let’s   add   new   numbers   to   keep   track.    Add   a   new   column,
second   from   the   left,   called R NUM    2 with   the   row   numbers   of the   tidy   data   set.   Output   the   first   10   rows,   and   the   dimensions,   of   the   data   set.
7.      Using   dot   points,   identify   what   types   of   variables   we   now   have   in   our   data   set,   i.e.,   “Quantitative   Discrete”,   “Quantitative   Continuous”,   “Categorical   Nominal”,   “Categorical   Ordinal”.      (Don’t   just   describe   what   data   type   they   are   in   the   tibble   —   you   need   to   think   about   the   type   of variable   in   the   context   of the   meaning   of   the   data.)   Make   sure   you   provide   some justification   for   your   choice   of variable   types.
•      Don’t just   provide   vague   statements,   but   be   very   concrete   about   describing   this   particular   set   of data.
8.      Now   it’s   time   to   tame   our   data.
•    Make   your   data   set   correspond   to   the   Tame   Data   conventions   on   page   3   of   Module   2.    You’ll   need   to use   your   answers   to   Q7. (Hint:       You might want to think about releveling some of your factors.    See    the 
Reminder Sheet.) 
•      Also   check   if   there   is   any   more   cleaning   that   is   required. If   so,   go   back   to   Q5 and   clean   it   there. (Hint: It might    be good to    check    one    last    time    if there    is    any    missing    data.       The is.na() command    on    the Reminder Sheet might come in handy.) 
Output   the   first   10   rows,   and   the   dimensions,   of   your   clean,   tidy   and   tame   data   set.9.   We   will   just   look   at   a   random   subset   of   your   data.    Setting   the   correct   seed   again,   take   a   random   sample   of
220   rows   from   the   dataset   in   Q8. Output   the   first   10   rows,   and   the   dimensions,   of   your   sample.
Note 
Use   this   random   subset   from   Q9 for   the   remainder   of   the   assignment.
10.    Insert   two   new   columns:
• goals:    The   team’s   number   of   goals   in   that   game    (put   this   between   the   columns   containing   the   total   score   and   the   number   of   behinds).
• goal acc:   The   proportion   of shots-on-goal   that   were   goals   (put   this   on   the   far   right   of the   data   set).Describe what type of variables these new columns represent   (“Quantitative   Discrete”,   “Quantitative   Contin-   uous”,   “Categorical   Nominal”,   “Categorical   Ordinal”).    Are   the   data   types   correct?    (Explain   your   answer.)   If   they   are   not   correct,   make   sure   you   change   them.
Output   the   first   10   rows,   and   the   dimensions,   of   the   data   set.
• If   you   discover   any   problems   with   the   data   here,   then   make   sure   you   go   back   and   start   again   from   Q5. You   may   want   to   check   that   the   calculations   resulted   in   the   correct   type   of output.
11.   We   would   like   to   know   the   probability   that   a   team   will   win   given   that   the   team   was   playing   at   home.    We   can   calculate   this   with   the   formula
Pr(team   wins   given   playing   at   home) = # games played at home/# games won by home team.
So   find   the   number   of rows   where   the   home   team   won   and   divide   it   by   the   number   of rows   where   the   team was   at   home.   Report   your   answer   with   the   correct   precision.
12.      Use   the   command summarise() to   create   a   new   tibble   called season totals containing   the   team   name,   the total   of   all   scores   by   that   team   for   each   game   over   the   season   and   the   average   accuracy   over   the   season. (Hint: you probably want to use group   by() .) Output   the   entire season totals data   set.
13.      Predict   which   teams   will   be   in   the   finals,   and   which   two   teams   are   likely   to   be   in   the   Grand   Final.    Make   sure   you   give   some   good   reasoning,   based   on   data, justifying   your   claim.
14.    Using   the season totals data   set   make   a   scatterplot   comparing   the   total   season   score   against   the   average accuracy   for   the   season.    Include   a   line   of   best   fit   on   your   plot.    Does   it   look   like   there   is   a   relationship   between these   variables?   Come   up   with   a   reason   for   why   the   relationship   (or   lack   of   a   relationship)   that   you   observe might   be   a   real   phenomenon,   and   not just   an   artifact   of the   data.
15. For   this   question   use   your   sampled   data   set   from   Q10. Produce   a   scatterplot   of total against goal acc,   with the   points   coloured   by   the   result   of the   match.   Make   sure you   put   your independent variable/predictor on   the   horizontal   axis,   and   give   a   brief explanation   of why   you   chose   that   variable   as   the   predictor.Hint: ggplot does some weird things with ordered factors, so if your plot doesn’t look particularly clear, then you    could try making a new data set specifically for plotting    by removing the    ordering.       Or    you    could also try the command scale   color brewer(palette = . . .) with the palettes Dark2, Set1 or Set2 to see what happens. 
16. Describe   any   relationship   between   score,   accuracy   and   result   that   you   see   in   the   scatterplot   of   Q15. 



         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
