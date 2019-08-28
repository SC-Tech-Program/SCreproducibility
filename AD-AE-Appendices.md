AD/AE Appendices Track
======================

In SC19, Artifact Description (AD) appendices were for the first time made mandatory for all technical papers, so SC19 was also the first SC to include an AD/AE Appendices Track.  The AD/AE Appendices Committee works, under the direction of its track chair, to conduct the review of all appendices submitted with technical papers. The review of appendices is a double-open process where committee members contact authors directly to help improve the appendices.

The responsibilities of the SC19 AD/AE Appendices Track Chair are:
 * Participate in the review of the new AD/AE merged forms.
 * Recruit a small committee who have shown special interest in the AD/AE appendices, or who were authors of papers that included a good appendix.
 * With the committee, implement a program of actions to mentor authors in the preparation of the appendices.
 * With the committee, help the Reproducibility Chair with the evaluation of submitted appendices in SC19.

The SC19 committee had ten active members.  Of SC19's 338 submissions, 96 were rejected before response leaving 242 appendices requiring review.  In SC19, the decision to reject before response was not communicated to the AD/AE Appendices Committee Track in time, so many of appendices for rejected papers were also reviewed.  On average, each reviewer reviewed 31 appendices.  139 of the 242 appendices were determined to be complete while 87 were incomplete and 16 were missing.  The review initiated at least 107 email conversations resulting in updates to nearly all the incomplete appendices.  Of the 16 papers with missing appendices, 11 appendices were added and judged complete, 3 papers were determined to not require an appendix as they were pure theory papers, and 2 papers were rejected after they elected not to provide the mandatory AD appendix, even after being warned of that outcome.  Eight candidates for Best Student Paper and six candidates for Best Paper had incomplete appendices before the review but had a complete appendix by the end of the revision period.  And finally, one candidate for Best Student Paper did not have the mandatory AD appendix before the review (and therefore was set to be rejected) but this review process helped the authors provide the complete appendix and stay in the running for Best Student Paper.

Overall the SC19 committee successfully completed their objectives, but there were significant "growing pains."  It is our hope that this report on lessons learned, missing tools, and suggestions for SC20 will improve the process and strengthen the overall value of the SC Reproducibility Initiative.  Any criticism below -- intended or perceived -- is given in the hope that it will be constructive and with the greatest respect for the hard work and dedication shown by all who participate in SC.  It is our sincere hope that these Lessons learned (LL) during SC19 are described below result in a much smoother SC20 review process.


Lessons Learned
---------------

  LL1. **The most important lesson learned was that new SC processes need a "dry run" well in advance of their intended deployment date.** SC19 experienced several major technical and organizational issues that could have been avoided if a dry run had been performed in advance of paper submission.  In many cases we didn't know what we needed until we needed it.  Whatever changes are made in SC20 need to be tested start-to-finish with ample time for Linkings and the SC committee to implement any missing pieces.  We strongly recommend a dry run in February 2020.

  LL2. Changes to the SC process must be communicated to Linklings in a clear and timely manner.  This is **crucial**.  It was assumed the Linklings staff were more aware of various SC processes -- especially processes new to SC19 -- than the Linklings staff possibly could have been.  For example, the process for reviewing the appendices was established in January but the mechanics of that process were not communicated to Linklings.  Hence, the tools for actually *doing* the review (i.e. downloading the appendix from Linkings and uploading the review to Linklings) were not implemented in Linklings until well after the review process should have been completed.  In order to deliver on their objectives, the AD/AE Appendices Committee were forced to build their own tools from a mixture of personal email accounts, local databases, Python scrips, and Google APIs.

  LL3. The timeline for appendices reviews needs to be clearly established and communicated to both Linklings and the AD/AE Appendices Committee. The SC19 AD/AE Appendices committee did not have access to the appendixes in Linklings until 25 April, just three days before reviews were due.  If the review timeline for the appendices had been communicated in a timely way, the AD/AE Appendices Committee would have requested access to the appendices much sooner and many of the problems we encountered would have been discovered earlier.  We recommend this timeline be established by the Technical Program Committee to coincide with the technical review.

  LL4. Double-open and double-blind workflows should be kept separate in Linklings.  Workflows for committees with double-open access to author-identifying information (e.g. the AD/AE Appendices Committee) should be implemented in Linklings as completely separate workflows from all other committees (e.g. the Technical Program Committee).  No part of the double-open workflows should not be visible in any way to someone performing a double-blind review.  Because the AD/AE Appendices workflow was implemented late, Linkings was forced to reuse parts of the technical program review workflow.  Upon being granted permission to view the appendices in Linklings (25 April), the AD/AE Appendices Committee discovered that author identifying information had been leaked to all double-blind paper reviewers in the form of the output of a script that captured environment variables for the AD Appendix.  We immediately asked Linklings to hide these fields from the double-blind review, but several papers had been reviewed at that point.  Furthermore, when the technical review concluded, fields that should have remained visible to the double-open AD/AE Appendices committee were automatically hidden.  This hampered our ability to identify papers eligible for the ACM Artifacts Available badge.  Implementing double-open and double-blind reviews as distinct workflows in Linklings will mitigate these issues.

  LL5.  The AD/AE Appendices Committee should be organized under the Technical Program Committee, not under the Reproducibility Committee.  Organizing the Appendices Committee under the Reproducibility Committee may seem logical, but in practice most of the Appendices Committee's needs, direction, and communication were driven from the Technical Program Committee.  Communication between the AD/AE Appendices Committee and the Technical Program Committee was dramatically improved when a direct line of communication was established ad-hoc.  Establishing this communication was key to delivering the appendices review.

  LL6. Email lists and aliases should be tested well in advance.  The AD/AE Appendices mailing list was advertised as the primary channel for authors to communication with the AD/AE Appendices Committee, but this mailing list was missing several committee members and included some email addresses that were no longer in service.  It was mid-May before we discovered this issue.  We also discovered (in June) that many Chinese email servers would block this email list.  It's highly likely that authors attempted to contact the SC19 AD/AE Appendices Committee but received no response.

  LL7. Email must be clearly established as the primary means of communication among SC committees.  Slack is not an email substitute!  Many people cannot use Slack due to company policy. During SC19 there were several communications issues caused by someone posing a message to Slack and assuming that everyone had seen it.  Please use email.


Tools Missing from the SC19 AD/AE Appendices Review
---------------------------------------------------

Because many of the tools needed for the AD/AE Appendix review were not implemented or were implemented too late, the AD/AE Appendices Committee were forced to create their own tools using a mixture of personal email accounts, Python scripts, and Google APIs.  Please contact john.christian.linford@gmail.com for copies of the scripts.  Specifically, the SC19 AD/AE Appendices Committee needed the following tools:

  * A tool for sending the results of the appendix review back to the authors.  In Linkings, the SC19 AD/AE Appendices committee had only a single check-box to indicate if the appendices were complete or incomplete.  There was no way to inform the authors of potential improvments an incomplete appendix!  We worked around this by building a software tool that parsed feedback from the appendices reviewers into a standard format and sent the results of the review via a private Gmail account to the paper authors.  However, some US government and Chinese government email servers will block personal communication from Gmail.  In that case we did our best to establish communication via other routes, but it was not always successful.

  * A tool for direct communication between the paper authors and the appendix reviewer with a history of communication.  The Linkings tools that enable paper shepherds to communicate with the authors of the shepherded paper would be perfect for this. For SC19, we worked around this by using our own personal email addresses.  We again encountered problems with certain email servers blocking personal email addresses.

  * A tool for tracking the AD/AE Appendix reviews separate from the technical reviews.  Because the appendix reviews were mixed-in with the technical reviews it was difficult to use Linkling's query/search/sort features to identify appendices that had (or had not) been reviewed.  We worked around this by downloading the Linklings paper list to a local database and building our own queries.

  * A tool for identifying papers eligible for certain ACM badges.  We worked around this by maintaining our own records and using custom queries.



Suggested Appendix Process for SC20
-----------------------------------

We suggest the following process for the SC20 appendices.  On the freeze date for paper content, strongly encourage the authors to include a draft of the AD/AE appendices.  Freeze the appendices when the technical review begins.  Reopen the appendices to changes during the revision period.


Conclusions
-----------

In spite of the difficulties described above, the AD/AE Appendices committee of 10 people reviewed over 300 appendices and initiated at least 107 email conversations.  139 appendices were determined to be complete while 87 were incomplete and 16 were missing.  Of the 16 papers with missing appendices, 11 appendices were added and judged complete, 3 papers were determined to not require an appendix as they were pure theory papers, and 2 papers were rejected after they elected not to provide the mandatory AD appendix.  One candidate for Best Student Paper did not have the mandatory AD appendix before the review (and therefore was set to be rejected) but this review process helped the authors provide the complete appendix and stay in the running for Best Student Paper.  The AD/AE Appendices Committee worked exceptionally hard and were able to deliver on their obligations.  We believe the reproducibility initiative should continue to be part of SC and that with the proper support and communication the AD/AE Appendices Committee will bring significant value to SC.  Please contact john.christian.linford@gmail.com for any further details on the SC19 AD/AE Appendices review.





