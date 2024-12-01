java c
ECM3422   –   Computability   and   Complexity 
Academic   Year:   2024/25
Title:    Continous   Assessment
Submission   deadline:   2024-11-27
This   assessment   contributes 20% of the   total   module   mark   and   assesses   the   following intended learning outcomes:
•    Module   Specific   Skills   and    Knowledge:
– explain what   is   meant   by   a   general   model   of computation   and work with   some   specific   examples   of   such   models;
– describe   the   mathematical   basis   of the   theory   of   computability   and   complexity;
•    Discipline   Specific   Skills   and    Knowledge:
– appreciate   the   power   of abstraction   to   support   a   general   understanding   of some   subject   matter;

– appreciate the   role of theoretical   understanding   in   underpinning disciplined   and   responsible   prac-   tice.
•    Personal   and    Key   Transferable   /   Employment   Skills   and   Knowledge:
– approach   problems   analytically   at   an   appropriate   level   of   abstraction.This   is   an individual assessment,   and   you   are   reminded   of   the   University’s   Regulations   on   Collaboration   and   Plagiarism.    You    must   avoid    plagiarism,   collusion   and   any   academic   misconduct   behaviours.      Further   details   about   Academic   Honesty   and   Plagiarism   can   be   found   at https://ele.exeter.ac.uk/course/ view.php?id=1957.
This   course   work   consists   out   of   two   questions.    You   can   get    up   to   100   marks   in   total   split   across   two   exercises:
1.    A   manual   simulation   of   a   multi   tape   Turing   Machine   (5h,   30   marks)
2.    An   implementation   of a simulator of   a   multi   tape   Turing   Machine   using   a   single   tape   Turing   Machine   (15h,   70   marks)The   CA   comes   with   template   python   files   which   you   can   download   from   the   assessment   section   on   the   ELE   page.   The   file   README.md   contains   detailed   instructions   on   how   to   run   the   tests. Before submitting your coursework make sure the project compiles and the tests provided in the template succeed. Implementations that cannot run the provided test suite, will receive zero marks.
Use of GenAI tools in Continous Assessment for ECM3422 - Computability and Complexity The   University   of   Exeter   is   committed   to   the   ethical   and   responsible   use   of   Generative   AI   (GenAI)   tools   in   teaching   and   learning,   in   line   with   our   academic   integrity   policies   where   the   direct   copying   of AI-generated   content   is   included   under   plagiarism,   misrepresentation and contract cheating   under definitions   and offences   in TQA   Manual   Chapter   12.3.   To   support   students   in their   use   of   GenAI tools   as   part   of their   assessments,   we   have developed   a category tool that enables staff to   identify   where   use   of   Gen   AI   is   integrated,   supported   or   prohibited   in   each   assessment.   This   assessment   falls   under   the   category   of   AI-supported.
You   can   find   further   guidance   on   using   GenAI   critically,   and   how   to   use   GenAI   to   enhance   your   learning, on   Study   Zone   digital. 
When submitting your assessment, you must include the following declaration, ticking all that apply: AI-supported/AI-integrated    use    is    permitted    in    this    assessment.       I    acknowledge    the    following    uses    of
GenAI   tools   in   this   assessment:
•    I    have   used   GenAI   tools   for   developing   ideas.
•    I   have   used   GenAI   tools   to   assist   with   research   or   gathering   information.
•    I    have   used   GenAI   tools   to   help   me   understand   key   theories   and   concepts.
•    I   have   used   GenAI   tools   to   identify   trends   and   themes   as   part   of   my   data   analysis.
•    I    have   used   GenAI   tools   to   suggest   a   plan   or   structure   for   my   assessment.
•    I   have   used   GenAI   tools   to   give   me   feedback   on   a   draft.
•    I   have   used   GenAI   tool   to   generate   image,   figures   or   diagrams.
•    I   have   used   GenAI   tools   to   proofread   and   correct   grammar   or   spelling   errors.
•    I   have   used   GenAI   tools   to   generate   citations   or   references.
•    Other:    [please   specify]
I   declare   that   I   have   referenced   use   of   GenAI   outputs   within   my   assessment   in   line   with   the   University   referencing   guidelines.Please note:    Submitting your work without an accompanying declaration, or one with no ticked boxes, will be considered a declaration that you have not used generative AI in preparing your work. If a declaration sheet cannot    be    uploaded    as part    of    an    assignment    (i.e.       at    the    start    of    an essay), students understand that by submitting their assessment that are confirming they have followed the assessment brief and guidelines about GenAI use. 
Instructions 
Task 1:    Simulating a Multi-Tape Turing Machine on a Single-Tape Turing Machine 
For   the   following   exercise   you   should   manually   simulate   a   given   multi-tape   Turing   machine   using   a   corre-   sponding   single-tape   Turing   machine.
Definition of the Multi-Tape Turing Machine 
The   multi-tape   Turing   machine   M   to   be   simulated   is   defined   as   follows:
M   =   (Q; Σ; Γ; δ   ; q0;   □; {q5   })
with
•    Q   =   {q0; ...; q5   }
•    Σ   =   {0; 1}
•      Γ   =   {0; 1; □   }
M   has   three   tapes   (and   three   read/write   heads).    Hence,   the   transition   function   has   the   form.:   δ   :   Q   × (Γ × Γ × Γ)   →   P(Q   ×   (Γ   ×   Γ   ×   Γ)   ×   ({L; R; N   } ×   {L; R; N   }   ×   {L; R;   N   }))   .
The triples   (Γ × Γ × Γ)   denote the   symbols   on the   first,   second,   and third tape   and   ({L; R; N   } ×   {L; R; N   } ×   {L; R; N   })   are   the   movements   of the   first,   second,   and   third   read/write   head.
The   transition   function   is   defined   as   follows:

Task Description  (30 marks) 
Assume   M,    is   a   corresponding single-tape Turing   machine   which   is   started   with   input   011010010For   this   task   you   need   to   determine   the   state   of   the   tape   for   M,      at   different   points   in   time.      The   state   of   the   tape   can   be   described   by   listing   the   elements   of Σ*    currently   on   the   tape. Note that you do not need to specify the state of M, nor the position of the head but only the state of the tape. 1.    What   will   the   tape   look   like   after   initialization   (i.e.,   when   M   reaches   q0   )?                                                                            (5   marks)2.    What   will   the   tape   look   like   when   M   reaches   q2   ?                                                                                                                                                                                                (5   marks)3.    What   will   the代 写ECM3422 – Computability and Complexity 2024/25Python
代做程序编程语言   tape   look   like   when   M   reaches   q3   ?                                                                                                                                                                                                (5   marks)4.    What   will   the   tape   look   like   when   M   reaches   q4   ?                                                                                                                                                                                                       (5   marks)5.    What   will   the   tape   look   like   when   M   reaches   q5   ?                                                                                                                                                                                                (5   marks)6.    What   will   the   tape   look   like   at   the   end   of the   execution?                                                                                                                                                                (5   marks)
Task 2:    Implementing a Simulator for    Multi-Tape Turing Machines using a given Single-Tape Turing Machine 
For this   exercise you   need to   implement   a   multi-tape   Turing   machine   using   a   given   single-tape   one.    To this   end   we   provide   you   with   a   Python   implementation   of   a   single-tape   Turing   machine.
Implementation of the Single-Tape Turing Machine 
The   single-tape   Turing   machine   is   implemented   in   class   TuringMachine   in   the   file   TuringMachine.py.   The   class   contains,   amongst   other   things,   the   following   elements:
•    A   string   variable   blank_symbol   which   stores   the   element   used   to   denote   a   blank   symbol.
•   A   constructor   __init__   which   initializes   the   machine.    It   takes   the   following   parameters:
– initial_state:   A   string   representing the   initial   state.
– final_states:   A   set   of strings   representing   the   final   states.
– head_position:   The   start   position   of   the   head   on   the   tape.
– tape_string:   A   string   representing   the   input.
•   A   method   is_final   which   takes   a   state   as   input   and   returns   true   if the   state   is   a   final   state.
•   An abstract   method transition with two   parameters:    a state and a   string.    The   method   is supposed   to   implement   the   transition   function.    It   must   return   a   triple   in   which   the   first   component   is   a   string   representing the   result state, the second   component   is   a   string   representing   the   output   character,   and   the   third   element   is   either   “L”,   “R”,   or   “N”   to   denote   the   movement   of the   head.
•    A   method   run   which   executes   the   machine   by   using   the   abstract   transition   method.
•   A   method   get_tape_string   to   return   a   formatted   string   of the   tape.
•    A   method   get_raw_tape   to   return   a   raw   representation   of   the   tape   in   which   leading   and   trailing   blanks   are   removed.
•    A   method   checkhead   which   takes   an   integer   and   checks   if   the   head   is   currently   on   that   position.   Counting   starts   from   the   first   non-blank   element   position.
•    A   method   is_blank   which   takes   a   string   and   checks   if   it   is   the   blank   symbol.Task Description  (70 marks) You   need   to   implement   the   multi-tape   Turing   machine   by   inheriting   from   the   class   TuringMachine.    We   provide   also   a template for this:    Class MTTuringMachine   in file MTTuringMachine.py.    The class   contains   the   following   elements:
•   A   constructor   __init__   which   takes   the   following   parameters:
– tapes:   An   integer   to   denote   the   number   of tapes.
– initial_state:   A string   to   denote   the   initial   state.
– final_states:   A   set   of strings   to   denote   the   final   states.
– tape_string:   A   string   to   denote   the   input.The   constructor   should   be   implemented   by   calling the   constructor   of the   single-tape   Turing   machine.
You need to implement this constructor. There is a TODO marker in the provided template which should be replaced by your implementation. 
•   An   abstract   function   transitionm   with   two   parameters:    a   state   and   a   tuple   of   strings.    This   method is   supposed   to   provide   the   implementation   of the   transition   function   for   the   multi-tape   machine   (i.e.   it   will    be    implemented    by    users   of   the   simulator).       This    function    is    provided    in   the   template   and should not be modified.
•   An   implementation   of   the   transition   method.   This   method   should   use   the   transition   function   of   the multi-tape   Turing   machine   (transitionm)   to   implement   the   transition   function   for   the   single-tape Turing   machine   (remember   that   transition   is   an   abstract   method   in   class   TuringMachine).
You need to implement this method. There is a TODO marker in the provided template which should be replaced by your implementation. 
The   class   can   use the   abc   library   for   abstract   methods   and the   re   library   for   regular   expressions   but should not use any other Python modules (libraries).Remark. We   provide   a   test   implementation   of   a   simple   multi-tape   Turing   machine,   extending   the   class   MTTuringMachine.   The   test   file   is   called   Tests   .py   and   contains   a   class   myTM   which   implements   a   multi-   tape   turing   machine   using   MTTuringMachine.      Moreover,   it   contains   a   class   TestStringMethods   which   provides   a   method   test_1   which   executes   a   possible   test   case.The   tests   can   be   executed   by   running   Tests   .py   using   Python   3.12.    We   strongly   recommend   that   you   use   it   to   test   if   your   implementation   fulfills   the    basic   functional    requirements. Implementations    that cannot be executed against this test suite will receive zero marks. Note   that   for   the   final   marking   we   will   use   additional   tests.
Marking scheme 
For   each   criteria   we    reward    marks    if   the    implementation    generally   satisfies   the   criteria,    and   we    provide   additional   marks   if   edge   cases   are   considered.
• Correct initialization:    The   single-tape   Turing   machine   is   properly   initialized   according   to   the   specifi-   cation   of the   multi-tape   Turing   machine   (general:    10   marks,   edge   cases:    10   marks)
• Correct    transition:    The   single-tape    Turing    machine   implements   the   correct   sequence   of   transitions   specified   by   the   multi-tape   Turing   machine   (general:   20   marks,   edge   cases:   20   marks)
• Correct finalization:    The   single-tape   Turing    machine    properly   finalizes   the   computation   (general:    5   marks,   edge   cases:    5   marks)

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
