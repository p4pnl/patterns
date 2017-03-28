    {%hyde

    title: "Privacy dashboard"
    excerpt: "An informational privacy dashboard can provide collected summaries of the collected or processed personal data for a particular user."
    status: draft
    type: pattern
    categories:
        - transparency
        - access
        - location
        - inform
        - provide        
    %}

[TOC]

### [Also Known As]
<!-- All other names the pattern is known by.-->

Privacy Mirrors / Minimal Information Asymmetry

## Summary
<!-- One short paragraph summarising the pattern.-->

Disclosure awareness is needed to adequately manage digital identity. Provide the user of a system with a high level overview on what personal data the system knows about, what access is given to others, and what kind of personal information can be deduced from this data. this is particularly useful when the data or services involved are numerous.

Supports [Access](Access), [Transparency and feedback](Transparency-and-feedback).

## Context
<!-- The situations in which the pattern may apply.-->

This pattern applies to all contexts in which a system processes the personal data of a user. This includes the collection and aggregation of such data, particularly that which:
- changes over time, 
- is processed in ways that might be unexpected, 
- is invisible or easily forgotten, or 
- where users have options for access, correction and deletion.

## Problem
<!-- The problem a pattern addresses, including a list of forces describing why a problem might be difficult to solve.-->

Users are frequently unaware of the personal data about them which a system processes. Moreover, they are often not aware what conclusions can be drawn about them from that data. Users may not remember or realize what data a particular service or company has collected, and thus cannot be confident that a service isn't collecting too much data. Users who are subjected to this information asymmetry may be surprised or upset when they discover the service's data collection practices. 

Without visibility into the actual data collected, users may not fully understand the abstract description of what types of data are collected; simultaneously, users may easily be overwhelmed by access to raw data without a good understanding of what that data means. Due to this, they either accept their data's undefined usage, or limit their disclosure, potentially more than needed, which could result in an poorer user experience.

How can a service succinctly and effectively communicate the kind and extent of potentially disparate data that has, is, or will be processed by a service? 

<details><summary> Forces and Concerns </summary>

Some aspects which illustrate the difficulty of this problem include:
- complacent ignorance from users,
- over and under-sharing,
- disinterest in details,
- notification fatigue, as well as
- the contextual appropriateness of information and notifications.

As in other access mechanisms, showing a user's data back to them can create new privacy problems. Implementers should be careful not to provide access to sensitive data on the dashboard to people other than the subject. For example, showing the search history associated with a particular cookie to any user browsing with that cookie can reveal the browsing history of one family member to another that uses the same computer. 

Also, associating all usage information with a particular account or identity (in order to show a complete dashboard) may encourage designers to associate data that would otherwise not be attached to the user account at all. Designers should balance the access value against the potential advantages of [Deidentification](Deidentification).

Even when provided with some level of transparency, such as lock icons for certificates, privacy coordination through color, or security warnings, often users overlook passive signs. An approach to this transparency which is both noticeable and yet unobtrusive is needed. One which is passively assertive. A purely technical solution is not appropriate, it must also consider physical and social contexts. This is because personal information has varying levels of sensitivity to users depending upon these contexts (for e.g. a closed room, or a close friend, are contexts in which some personal information may be considered less vulnerable).
</details>

## Solution
<!-- A concise description of how the pattern addresses the problem.-->

An informational privacy dashboard can provide collected summaries of the collected or processed personal data for a particular user. While access to raw data may be useful for some purposes, a dashboard provides a summary or highlight of important personal data. Seek to make the data meaningful to the user with examples, visualizations and statistics. Methods, mechanisms, and interfaces which reflect the history, flow, state, and nature of processed personal data which may otherwise have been hidden are also encouraged.

Where users have choices for deletion or correction of stored data, a dashboard view of collected data is an appropriate place for these controls (which users may be inspired to use on realizing the extent of their collected data).

In short, a dashboard answers the common user question "what do or will you know about me?" and does so in a way that the user can understand and take appropriate action if necessary.

### [Structure]
<!--A detailed specification of the structural aspects of the pattern. A class diagram if applicable.-->

A variation of the privacy dashboard, Privacy Mirrors, focuses on five characteristics in particular:
- history, of data flows;
- feedback, regarding the state of their physical, social, and technical environment;
- awareness, enabled by the feedback;
- accountability, from these; and
- change, enacted by the users.

<details><summary> History </summary>

Logging is possible in technical systems from as little to as much granularity as desired. Whatever is kept needs to have been done so bearing in mind the social implications, i.e. the contexts, which may be important to a user's privacy. Who was involved in the processing, where was it processed, when, how, why, etc. are relevant.  

  The past must be summarized in a way which is easy to understand, but still detailed enough to identify less obvious risks. What information is relevant to different users as opposed to that which is seen as unnecessary noise? What isn't socially acceptable to record? How long must this be kept, should it deteriorate or simply vanish?
</details>

<details><summary> Feedback </summary>

Logging is of little (or detrimental) use if not transparent and appropriately accessible. There needs to be a way to disseminate this history, state, and flow information to the users without inducing notification fatigue and without exposing information which is not contextually acceptable. Visual cues may be less distracting than the use of other senses, and capable of conveying much more information. However, some contexts may call for more distracting notification. A user should be able to choose whether, how much, and by what means they are notified - as some people have higher tolerances, or different tolerances, for distraction than others.

A distinction is suggested between notifications which require 'glancing', 'looking', or 'interacting'. Examples of these in an Android system are toast notifications (ambient display), heads up notifications (in the status bar), and pop up notifications, respectively. Ideally, each level will be available to cater to a user's personal preference. Information about a certain context should by default be found in the location where users would naturally look for it.

In feedback, how should different senses be addressed, to what level, where should it be shown, for how long, etc. These are aspects which should ideally be user configurable, with reasonable defaults. This should cater to what each user determines is important.
</details>

<details><summary> Awareness </summary>

This concept includes the user's knowledge about how they feature in the system, how others feature with regards to the user's personal data, as well as what capabilities and constraints entities are given. The level of information and notification to convey depends on the user, as some will want more detail than others - meeting this balance will make the user more comfortable with their involvement. 

This awareness can be divided amongst the three domains:   
- Social: Notable usage patterns on access, being able to correlate this with others and encourage better decisions. 
- Technical: Understanding the limitations of the system, and the capabilities if used correctly, to use the system more effectively. Users should understand the flow, state, and history of their personal data in the system.
- Physical: Having regard for the repercussions of their physical state, including location, being perceivable by the system.

In maintaining awareness, one difficulty is in adequately informing users of the flows, history, and states of more complex systems. Meeting the balance between overwhelming users and underwhelming them can be difficult.
</details>

<details><summary> Accountability </summary>

In a ubiquitous system, interpersonal information is something which should ideally be traceable to show who can access, and has accessed, what. In order for social governance to take place, people should be held accountable for what they do. When personal data is accessed, it should be clear who did so, and when - to both the person concerned and the one doing the accessing. Other matters such as how it was accessed, where from, or why, are also subject to the social norms and contexts placed on these aspects by those concerned. This 'you-know-that-I-know-that-you-know' effect controls the (mis)use of shared personal information.

Another balance to make is how much accountability is necessary. Too much exposure of usage may create tension, while too little may do the same. Being able to reliably link usage to an individual is also a matter to consider.
</details>

<details><summary> Change </summary>

The social norms brought into the foreground, or created through the previous steps will bring about changes in usage. Being able to anticipate repercussions for actions, will cause users to think more carefully about what they reveal and what they access, as well as how (often), when, why, etc. If a user can determine that certain changes to information flow will be overall beneficial, the user may decide to act on those changes. This applies to both the user's needs, and that of the those around them.

Understanding the resulting effect of sharing or controlling information will help users find a level which suits them. Although some may retreat in-wards upon realizing the consequences of over-sharing, or over-share when the consequences of doing so are not immediately apparent. This is why meeting the balance is important. There is also the matter of outliers, where some users will not be as comfortable or as uncomfortable as the majority. Therefore, having the means to share less or more than others is important.
</details>

### [Implementation]
<!--Guidelines for implementing the pattern; code fragments; suggested PETS; policy fragments.-->

Implementing this pattern is a matter of providing logging, reporting, and other informational access and notifications on user-selected/filtered, appropriately defaulted, relevant usage data. The data provided to the notified users should not intrude on other users' sensitive information, apart from the activities which involve the notified users.

The right balance needs to be met, both in the selected defaults and in the minimum and maximum levels available to the users in settings. The settings should be found easily, as should additional information. Balanced defaults can be determined from identified norms among users, while minimums should cater to the least interested and maximums to those most interested in their data's usage. 

Users should ideally be able to choose the medium for the notifications, and for information retrieval, which best suits them. Candidates include email, push notifications on mobile devices, or simply from the dashboard itself.

An effort may be made to slowly introduce users to this system. For example, starting out more privately and then gradually revealing future information so that users have time to adjust their usage. This way users are less likely to portray an undesirable usage pattern.

These correlations may also be stored in a secure way, so that they cannot be viewed arbitrarily by backend users. If users are given assurances about what information can be seen by who, including backend users, they will be more willing to make use of the information and notification system.

## Consequences
<!--The advantages (benefits) and disadvantages (liabilities) of applying the pattern.-->

Advantages:
- Users are less likely to portray a negative usage pattern if they are aware of the correlation of their actions to it. This results in a more positive user experience once adjustments have been made. In some cases, this can increase productivity, and or efficiency in using the system.

Disadvantages:
- Initial discovery of the way they appear from the outside may lead users to retreat into themselves and disclose little to no information, cease using the system, and or call for their usage to be erased. This can be mitigated by introducing users to the system in stages and as soon as possible.
- Even if introduced slowly, users may be dissatisfied with their usage pattern as it appears to the system (and any authorized backend users). These correlations should ideally be difficult (or impossible) to retrieve by anyone other than the user in question.

<!--### [Constraints]-->
<!-- limitations as a consequence of applying the pattern.-->



## Examples
<!--Motivational example to see how the pattern is applied.-->

* _Google Privacy Dashboard_

![Google Dashboard Latitude](media/images/Google_Dashboard_Latitude.png)

The [Google Dashboard](https://google.com/dashboard) shows a summary of the content stored and/or shared by many (but not all) of Google's services (Latitude, Google's location sharing service, is shown above). For each service, a summary (with counts) of each type of data is listed, and in some cases an example of the most recent such item is described. An icon signifies which pieces of data are public. Links are also provided in two categories: to actions that can be taken to change or delete data, and to privacy policy / help pages.

[Google Accounts: About the Dashboard](http://www.google.com/support/accounts/bin/answer.py?answer#162744)

<!--### [Known Uses]-->
<!-- Pointers to various applications of the pattern.-->



## See Also
<!-- Any pointers to relevant information, not contained in the subfields below.-->

Dashboards are a widely-used pattern in other data-intensive activities for providing a summary of key or actionable metrics. See: _external references needed here_

<!--### [Related Patterns]-->
<!-- Supporting and conflicting patterns-->



### [Sources]
<!-- References to the original source of the pattern.-->

N. Doty & M. Gupta, (2003). “Privacy Design Patterns and Anti-Patterns Patterns Misapplied and Unintended Consequences,” 1--5.

D. H. Nguyen and E. D. Mynatt, (2002). “Privacy Mirrors : Understanding and Shaping Socio-technical Ubiquitous Computing Systems', pp. 1--18.

S. Romanosky, A. Acquisti, J. Hong, L. F. Cranor, and B. Friedman, (2006). “Privacy patterns for online interactions,” Proceedings of the 2006 conference on Pattern languages of programs - PLoP ’06, p. 1.

C. Bier & E. Krempel, (2012). “Common Privacy Patterns in Video Surveillance and Smart Energy,” In ICCCT-2012 (pp. 610--615). Karlsruhe, Germany: IEEE.

#### See Also
<!-- A design pattern in developing successful privacy; C14 -->

E. S. Chung et al., (2004). “Development and Evaluation of Emerging Design Patterns for Ubiquitous Computing,” DIS '04 Proceedings of the 5th conference on Designing interactive systems: processes, practices, methods, and techniques, pp. 233--242. 

<!-- References Chung et al. with additional detail -->

H. Baraki et al., (2014). “Towards Interdisciplinary Design Patterns for Ubiquitous Computing Applications,” Kassel, Germany.

<!-- Analogy citing original, Section 3.3.5 -->

G. Iachello and J. Hong, (2007). “End-User Privacy in Human-Computer Interaction,” Foundations and Trends in Human-Computer Interaction, vol. 1, no. 1, pp. 1--137.


<!--## General Comments-->
<!-- Separate discussion on the pattern.-->



<!--## Tags-->
<!-- User definable descriptors for additional correlation.-->


