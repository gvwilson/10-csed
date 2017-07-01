# Ten Simple Rules for Teaching Programming

**Neil C. C. Brown<sup>1</sup>, Greg Wilson<sup>2</sup>**

1. King's College London / neil.c.c.brown@kcl.ac.uk
2. Rangle.io / gvwilson@third-bit.com

## Introduction

Computing is a younger discipline than mathematics, physics, or biology,
and there have been correspondingly fewer studies of how best to teach it.
However,
there is a growing body of evidence about what works and doesn't in programming education.
This paper presents ten simple rules that should be the foundation of any course,
formal or informal.

## 1) There's no geek gene (Patitsas et al)

Guzdial refers to the belief that some people are born programmers and others aren't
as [computing's most enduring and damaging myth][guzdial-geek].
Our first and most important rule is that this is wrong:
competence at programming is not innate,
but is rather a learned skill that can be acquired and improved with practice.

The most powerful evidence for this comes from [Patitsas et al][patitsas].
They examined grade distributions in introductory computing courses at a large university,
and found that only 5.8% were actually multi-modal.
More damningly,
they found that computer science faculty were more likely to see distributions as bimodal
if they thought those grades came from a programming class
than if they believed the grades came from some other kind of class,
and that those faculty were even more likely to see the distributions as bimodal
if they believed some students are innately predisposed to do well in computer science.

Beliefs such as this are known to have powerful effects on education outcomes [FIXME][fixme-outcomes].
If instructors believe that "some kids get it and some kids don't",
they will (consciously or unconsciously) invest less in those whom they put in the second category.
When combined with cultural stereotypes about who is and isn't a "natural programmer",
the downward spiral of under-achievement that results from differential attention
may be partly responsible for the gender imbalance in computing.

## 2) Use live coding

Rather than using slides,
instructors should write programs in front of their learners [FIXME][fixme-live-coding].
This is more effective for multiple reasons:

1.  It enables instructors to be more responsive to "what if?"
    questions. Where a slide deck is like a railway track, live coding
    allows instructors to go off road and follow their learners'
    interests.

2.  It facilitates unintended knowledge transfer: students learn more
    than the instructor consciously intends to teach by watching *how*
    instructors do things.

3.  It slows the instructor down: if they has to type in the program
    as they go along, they can only go twice as fast as their
    learners, rather than ten-fold faster as they could with slides.

4.  Learners get to how instructors diagnose and correct
    mistakes. Novices are going to spend most of their time doing
    this, but it's left out of most textbooks.

5.  Watching instructors make mistakes shows learners that it's all
    right to make mistakes of their own.  Most people model the
    behavior of their teachers: if the instructor isn't embarrassed
    about making and talking about mistakes, learners will be more
    comfortable doing so too.

Live coding does have some drawbacks, but with practice, these can be
avoided or worked around:

1.  Instructors can go too slowly, either because they are not good
    typists or by spending too much time looking at notes to try to
    remember what they meant to type.

2.  Typing in boilerplate code that is needed by the lesson, but not
    directly relevant to it (such as library import statements), can
    distract learners from the intended thrust of a lesson.  As
    [Willingham][willingham] says, "Memory is the residue of thought";
    if the instructor spends their time typing boilerplate, that may
    be all that learners take away.

## 3) Have students make predictions

- Being wrong stings!  Which is good.  Easy to brush it off if you haven't made prediction public.
- Research on how students misremembered physics demos afterwards.
- More engaging if you have to have to think about it and take an action.

## 4) Use peer instruction

No matter how good teachers are,
they can only say one thing at a time.
How then can they clear up learners' many different misconceptions
in a reasonable time?

The best method developed so far is called peer instruction.
Originally created by Eric Mazur at Harvard [FIXME][fixme-mazur],
it has been studied extensively in a wide variety of contexts,
including programming [Porter2013][porter] and [cutts][fixme-cutts].
In simplified form,
peer instruction proceeds in three phases

1. The instructor gives learners a brief introduction to the topic.
1. The instructor then gives learners a multiple choice question
   that probes for misconceptions rather than simple factual recall.
1. Learners then vote on the answer to the question.
   * If they all have the right answer, move on.
   * If they all have the same wrong answer,
     the instructor addresses that specific misconception.
   * If they have a mix of right and wrong answers,
     they are given several minutes to discuss those answers with one another
     in small groups (typically 2-4 students)
     and then reconvene and vote again.

Peer instruction is essentially
a way to provide one-to-one mentorship in a scalable way.
Group discussion significantly improves learners' understanding
because it forces them to clarify their thinking,
which can be enough to call out gaps in reasoning.
Re-polling the class then lets the instructor know if they can move on,
or if further explanation is necessary.
While it significantly outperforms lecture-based instruction in most situations,
it can be problematic if ability levels differ widely
(as they often do in introductory programming classes
because of varied prior experience).
The practice advocated in our next rule can be used to mitigate this.

## 5) Use pair programming

- Evens out differences in ability
- Both parties learn something
  - The weaker gets individual instruction
  - The stronger learns from teaching
- McDowell et al 2006

## 6) Use worked examples with labelled subgoals

- Lets you give students many different specific problems, while making clear the higher-level isomorphisms between the problems.
- Without subgoal labels, learners don't always see the spirals in a spiral curriculum.
- There is a complex result in the Morrison, Guzdial work about writing your own labels.  May be too intricate to include?

## 7) Start with blocks

- Evidence generally points to blocks being better than text.
- This can conflict with context though, and you may encounter resistance from learners (inauthenticity, etc)

## 8) Stick to one language

A principle that applies across all areas of education is that transference only comes with mastery [FIXME][fixme-transference]:
novices don't yet have a working mental model of the problem domain,
and so are unable to distinguish general principles from the specifics of particular problem instances.
While an experience programmer can,
for example,
take what they know about loops and function calls in one language
and re-use that understanding in a language with a different syntax or semantics,
a newcomer does not yet know which elements of their knowledge are central
and which are accidental.

Courses should therefore stick to one language until learners have progressed far enough with it
to be able to distinguish the forest from the trees.
Attempting to force transference too early---i.e.,
requiring them to switch from Python to JavaScript in order to do a web programming course
early in their education---will confuse learners and erode their confidence.

## 9) Use authentic tasks

[Guzdial et al][guzdial-media] found that having learners manipulate images, audio, and video
in their early programming assignments
increased retention in two senses:
learners remembered more of the material when re-tested after a delay,
and were more likely to stay in computing programs.
Their studies,
which have since been replicated [FIXME][fixme-media-comp-replication],
are consistent with findings from other areas of educational research [FIXME][fixme-authentic-tasks]:
learners find *authentic tasks* more engaging than abstracted examples.

FIXME: ITiCSE report says context makes no difference to task performance.

One caution is that context can inadvertently exclude some people while drawing others in.
For example,
many educators use computer games as a motivating example for programming classes,
but some learners may associate them with violence and racial or gender stereotypes.

## 10) Don't just code

Our final rule for teaching programming is that you don't have to program to do it.
Between syntax, semantics, algorithms, and design,
examples that seem small to instructors can easily overwhelm novices.
Breaking the problem down into smaller single-concept pieces can reduce the cognitive load to something manageable.

For example,
a growing number of educators are including Parsons Problems in their pedagogic repertoire [FIXME][fixme-parsons].
Rather than writing programs from scratch,
learners are given the lines of code they need to solve a problem,
but in jumbled order.
Re-ordering them to solve the problem correctly allows them to concentrate on mastering control flow
without having to devote mental energy to recalling syntax
or the specifics of library functions.

## Conclusion

Like anything involving human subjects,
studies of computing education must necessarily be hedged with qualifiers.
However,
we do know a great deal,
and are learning more each year.
Venues like [SIGCSE][sigcse],
[ITiCSE][iticse],
and [CSER][cser]
present a growing number of rigorous, insightful studies
with immediate practical application.
Future work may overturn or qualify some of our ten simple rules,
but they form a solid basis for any educational effort.

[fixme-authentic-tasks]: cite-value-of-authentic-tasks
[fixme-cutts]: cutts-ref-for-peer-instruction
[fixme-live-coding]: cite-live-coding
[fixme-mazur]: cite-mazur-peer-instruction
[fixme-media-comp-replication]: cite-media-computing-replication
[fixme-outcomes]: cite-belief-in-innate-ability-shaping-outcomes
[fixme-parsons]: cite-parsons-problems
[fixme-transference]: cite-on-general-knowledge-transfer
[guzdial-geek]: https://cacm.acm.org/blogs/blog-cacm/189498-top-10-myths-about-teaching-computer-science/fulltext
[guzdial-media]: FIXME
[patitsas]: http://www.cs.toronto.edu/~sme/papers/2016/icer_2016_bimodal.pdf
[porter]: porter-et-al-peer-instruction
[sigcse]: FIXME
[willingham]: https://www.amazon.com/Why-Dont-Students-Like-School/dp/047059196X/
