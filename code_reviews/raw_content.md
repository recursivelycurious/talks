Code Reviews
------------

_____


Disclaimer:
- I knew that. Good. How well do you practice it? What do you do to socialize it? To automate it?
- Sending me an MR because of this talk? If I am not prominent in git annotate, this is almost certainly unadvised.
- Thank you in advance for gentle reminders when I go astray.

_____

Big picture:
- Code is for humans. Machines read bits.
- Code is read *many* more times than it is written.
- Working code that is opaque will consume time and create bugs.
- Automation can make review time more effective and more efficient.
  BUT, when automation can genuinely real code review, we will be unemployed.
_____


Question: How might code reviews be the most valuable thing we can do as F5 developers?


Answer: 

Code reviews is where we learn the most about what kind of development is accepted by our peers.

It is also where we get to work with one another to define our culture.

_____

Vision:

Authors and Reviewers should be better software engineers at the end of every review.

_____


The case against code reviews
- Reject poor practices, but not code reviews as a whole.
- Present workplaces using extreme programming, such as peer programming.
- Clever reverse psychology titles.

Conclusion: Code reviews are good when done correctly.

_____


What code reviews should not address (change this to minimum take away)
- Anything that *is* done by an automated test.
  - Can be done by an automated tool just means it needs to be done by one.
- Changes at odds with the timing/objective of the review.
  - Design feedback (well in advance of merge)
  - Merge or other Gating (sufficiently in advance of the decision to gate)
  - Knowledge Sharing (typically after code is in - “here is what was done, is this sane?”)
- Pick specific reviewers
  - Shotgun is not effective
  - use git

_____


Great Resources
- Got 10 minutes? Tim Peterson from Atlassian
- Invest an hour? Trisha Gee from JetBrains
- Big on Static Analysis? Jones & McCabe from SmartBear

Thank you and good morning...

Next level.


_____


Highlights, from research.


_____


Peterson:
- Be mindful of coherence - all of the changes under review should fit into a whole.
- Be mindful of scope - too small, all we see are nits, too big we miss everything.
- Reviews find bugs, and fewer reviewers find MORE bugs. (Cliff at 5).
- Fewer reviewers spend more time; many reviewers means no one actually reviews.
- Use git to identify reviewers. (Who’s code are you changing or removing?)
- Move discussions into code (comments, renames).
- Build, and review, policy as a team in sprint review *and enforce it*.
- Use screen casts for UI/UX and product review


_____


Lee
- Our job is to help get GOOD code in, not to find problems.
- Anti-patterns that undermine the value of code reviews and indicate a poor review process.

- Why
- When
- Who
- Where
- What
- How

_____


- Why?
  - Standards must be listed.
  - Bugs (do all the automated things first)
  - Knowledge sharing (cannot be automated) problem / solution
  - Comprehension (cannot be automated)
  - Complete (tests, yes, but the test also have to be reviewed)
  - Collaborate on design, particularly asynchronous


_____

- When?
  - When should it be started? Timing as mentioned above.
  - When is it complete?

_____

- Who?
  - Gatekeeper?
  - Lead or senior?
  - Juniors?
  - Who signs off?
  - Who breaks deadlocks?

_____

- Where?
  - Pairing rather than reviews.
  - Sit together and walk through (Zoom counts).
  - Demo?
  - Async: branches, tools (including gitlab MR) - more common in InfoSec and Compliance

_____

- What?
  - Depends on everything above... and
  - This gets HUGE
  - Do what cannot be automated (but only if it has been automated).
  - Understand constraints (particularly for security).
  - For gates, have specific check list.


_____


- How?
  - Automate everything you can.
  - Small (digestible).
  - Provide context; commit messages, MR description.
  - Respond in a timely fashion.
  - Comments should be specific and constructive.
  - Address the code, not the author.
  - Include praise.
  - Make sure the expected action is clear. Fix it? Open an issue?
  - “Raise concern” rather than “reject”.

_____


Deep breath.

This is a LOT of information. 
- Code reviews are complex.
- Technological and Social factors. 

How can we organize it?

3.a. BeF5

Owners
Thrive
Customer Needs
Zoom Out
Speed

Remember our question...

We are building a culture in addition to a product.

Thesis:
- Good code reviews are necessary, but not sufficient, for high quality code on this project.
- Poor code reviews (no code reviews are poor code reviews) are sufficient for poor quality.

Values again... this time in terms of code review.

Some suggestions:
- Authors should organize their commits in terms of problem, solution, tests, [analysis].
- Authors should find reviewers as early as possible for the type of review they need, design/gate.
- Assignees should be used when an author or reviewer believes the assignee should gate the review.
- Don’t use groups. Communicate with individuals.
- These and/or other standards should live in a contributing.md.
- Use merge bot as an approver.

THANK YOU.

Before we begin:
- Should I make Michael a reviewer on foo? (Almost certainly no... we’ll cover how to pick reviewers).
- I knew that. Great! How effective are you at it? How well do you teach it to others? What improvements have you made?

Some great resources:
- aka, tldr ;)

Our Objectives Today:
- In Opposition to Code Reviews
- 

What is the objective of the review?
- Gating
- Knowledge Sharing
- Design feedback

OR
- Complete
- Usable
- Maintainable
- Extensible
- 


What are our objectives as reviewers?
- NOT to find things wrong.
- Help the author get the best solution to the problem in terms of the constraints above.




From Lee’s intro:
- it works
- its tested
- it satisfies non functional requirements

Finding the right reviewer:
- Start the conversation before you open the Merge Request
- Its okay to say no. Be clear about why and help the author find another reviewer.
- Use assignees to designate a gatekeeper. Do this more than once if that works (lead, architect) 

DATA
——

Fewer Reviewers Find more defects:
- five is the cliff?

Fewer reviewers spend more time:
- inversely linear

“Poor quality is cheaper until the end of the coding phase. After that, high quality is cheaper.”

Data from IBM. Project that include “inspection” plateau, then rise slowly in terms of cost after initial implementation. Those that don’t spike and rise faster. 

Use Git:


Use GitLab:
- @mention
- settings
- noise


Use MergeBot:


Get it done:
- Review live
- Make time

Scope:
- 30 minutes: this includes time to comment.


Build policy as a team:
- should be part of the sprint review
- enforce it.

Not just for code:
- screen shots? 
- demos
- monosnap
- giphy
- screenflow

Staged environment:
- link to and leave up



How to review:
- What are the best tests?
  - Are they written? Can they be?
- Git

Good discussions on the MR highlight good comment opportunities.


Sources
-------
Trisha Gee
Code Review Best Practices - https://www.youtube.com/watch?v=a9_0UUUNt-Y
What To Look For In A Code Review - https://leanpub.com/whattolookforinacodereview


Capers Jones & Tom McCabe of smart bear
https://www.youtube.com/watch?v=T6IKMBPMCL8&list=PLrA5ciulugn8HjjGVY72i5eoF-qv9xqbB

Tim Pettersen - Senior Dev, Atlassian
https://www.youtube.com/watch?v=fatTnX8_ZRk


[ Get code that adds value checked in. ]
[ Reduce cognitive load for devs, users. ]
[ Increase leverage. ]
[ Reduce complexity (introduce abstractions). ]

Context
- Are the commits coherent in terms of problem, solution?
- Is this clearly stated in the commit message?
  - label fixup commits


- Don’t look for things a machine can look for (unless the machine isn’t)
- Design Principles
- Design Patterns
- Code Location
- Does it Re-use existing code where it can?
- Can it be re-used in turn? (Does it need to be?)
- Do the names make sense?

- Is this production ready? (Test data, test data base)

- Is every loose end called out and actionable?

Tests:

- are there tests?
- Should there be? (Python over bash)
- Do the tests tell you the requirements?
  - Could you reconstruct the code from the tests?
- Are the key requirements covered? 
- Are unhappy paths covered?
- Are there tests for known limits?
- Where are the test boundaries? How are they communicated?
- Have a test? Add a commit / open an additional review (another benefit of branches).
- bug fixes:
  - red to green.
  - tests run in loops?
  - tests shuffled?
- clean up / avoid false negatives

Performance and resource management:
- db calls
- network calls
- excess locks
- leaks
- races
- clean up? (Close connections / channels )
- unbound data structure?

