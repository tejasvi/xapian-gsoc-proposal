.. This document is written in reStructuredText, a simple and unobstrusive
.. markup language.  For an introductiont to reStructuredText see:
.. 
.. http://www.sphinx-doc.org/en/master/rest.html
.. 
.. Lines like this which start with `.. ` are comments which won't appear
.. in the generated output.
.. 
.. To apply for a GSoC project with Xapian, please fill in the template below.
.. Placeholder text for where you're expected to write something says "FILLME"
.. - search for this in the generated PDF to check you haven't missed anything.
.. 
.. See the [wiki:GSoCProjectIdeas ideas list] for some suggested project ideas.
.. You are also most welcome to propose a project based on your own ideas.
.. 
.. From experience the best proposals are ones that are discussed with us and
.. improved in response to feedback.  You can share draft applications with
.. us by forking the git repository containing this file, filling in where
.. it says "FILLME", committing your changes and pushing them to your fork,
.. then opening a pull request to request us to review your draft proposal.
.. You can do this even before applications officially open.
.. 
.. IMPORTANT: Your application is only valid is you upload a PDF of your
.. proposal to the GSoC website at https://summerofcode.withgoogle.com/ - you
.. can generate a PDF of this proposal using "make pdf".  You can update the
.. PDF proposal right up to the deadline by just uploading a new file, so don't
.. leave it until the last minute to upload a version.  The deadline is
.. strictly enforced by Google, with no exceptions no matter how creative your
.. excuse.
.. 
.. If there is additional information which we haven't explicitly asked for
.. which you think is relevant, feel free to include it. For instance, since
.. work on Xapian often draws on academic research, it's important to cite
.. suitable references both to support any position you take (such as
.. 'algorithm X is considered to perform better than algorithm Y') and to show
.. which ideas underpin your project, and how you've had to develop them
.. further to make them practical for Xapian.
.. 
.. You're welcome to include diagrams or other images if you think they're
.. helpful - see http://www.sphinx-doc.org/en/master/rest.html#images for how
.. to do so.
.. 
.. Please take care to address all relevant questions - attention to detail
.. is important when working with computers!
.. 
.. If you have any questions, feel free to come and chat with us on IRC, or
.. send a mail to the mailing lists.  To answer a very common question, it's
.. the mentors who between them decide which proposals to accept - Google just
.. tell us HOW MANY we can accept (and they tell us that AFTER student
.. applications close).
.. 
.. Here are some useful resources if you want some tips on putting together a
.. good application:
.. 
.. "Writing a Proposal" from the GSoC Student Guide:
.. https://google.github.io/gsocguides/student/writing-a-proposal
.. 
.. "How to write a kick-ass proposal for Google Summer of Code":
.. http://teom.wordpress.com/2012/03/01/how-to-write-a-kick-ass-proposal-for-google-summer-of-code/

======================================
Integrating WordNet into Xapian
======================================

About You
=========

 * Name: Tejasvi S Tomar

 * E-mail address: tstomar[at]outlook.com

 * IRC nickname(s): tstomar

 * Any personal websites, blogs, social media, etc: http://tejasvi.github.io (stem blog)

 * github URL: http://github.com/tejasvi

 * Biography: 
   
   I am enthusiastic about technology and its impact on people lives.
   Currently I'm pursuing bioengineering as an undergrad. The field of computational biology, genomics, and neuroscience interest me the most. I've been fascinated with computers and biology since I was a kid. And ever since wanted to work in this interdisciplinary field. Of late, I'm also intrigued with AI, augmented reality and philosophy behind them. I look forward to contribute in making of the exciting future ahead.
   
   When I'm off screen, I have many and varied interests. Currently I swim and play water sports. I'm an avid book reader and occasionally write. And if there is time at hand I engage in philosophy too.  

.. Tell us a bit about yourself.


Background Information
----------------------

.. The answers to these questions help us understand you better, so that we can
.. help ensure you have an appropriately scoped project and match you up with a
.. suitable mentor or mentors.  So please be honest - it's OK if you don't have
.. much experience, but it's a problem if we aren't aware of that and propose
.. an overly ambitious project.

**Have you taken part in GSoC and/or GCI (https://codein.withgoogle.com/) and/or
similar programmes before?  If so, tell us about how it went, and any areas you
would have liked more help with.**

I wish I were aware of GCI earlier. However this is my first chance to apply for GSoC.

**Please tell us about any previous experience you have with Xapian, or other
systems for indexed text search.**

Nothing major projects I worked on before involved search systems. Though I had abstract idea of workings of search engine which is more concrete now after working with Xapian.

**Tell us about any previous experience with Free Software and Open Source
other than Xapian.**

I came accross linux as my eight years old PC started slowing down. Since then I have tried tens of distros and various utilities present within. Though my knowlege expanded more or less within the scope of general computing and only recently the scope has broadened to development. And I'm loving it so far and excited to to get deep into it.

**What other relevant prior experience do you have (courses taken at college,
hobbies, holiday jobs, etc)?**



**What development platforms, tools and methods do you prefer to use?**

Currently I use vscode as the editor. On the OS side I've tried plethora of configurations and found Ubuntu with KDE to suit me well. However I'm not reluctant to try out new tools if the situation demands.

**Have you previously worked on a project of a similar scope?  If so, tell us
about it.**

Though none matching same scope, I have completed a moderately sized robotics project. The objective was to balance balls on movable plate using microcontroller. The code involved was in C++ and algorithm for balancing derived from a research article. The idea of implementation was to get coordinates of ball and predict the tilt of the plate based upon current, past, and target coordinates of the ball.

Project repo: https://github.com/tejasvi/ballet-of-bots 

**What timezone will you be in during the coding period?**

UTC +5.5

**Will your Summer of Code project be the main focus of your time during the
program?**

Yeah, it will be for sure.

**Expected work hours (e.g. Monday–Friday 9am–5pm UTC)**

I will spend at least six hours a day. Also I would prefer to spread out my work equally over week days. It translates to at least 42 hours of work for a week. Besides, I'll have extra 3-4 hours to commit during summer break or on holidays. 

**Are you applying for other projects in GSoC 2019?  If so, with which
organisation(s)?**



.. We understand students sometimes want to apply to more than one org and
.. we don't have a problem with that, but it's helpful if we're aware of it
.. so that we know how many backup choices we might need.

Since here I found skillset required to be most holistic, I would prefer to work exclusively with Xapian for now.

Integrating WordNet into Xapian
============

WordNet is a lexical database which will provide additional insight to analyse relevance of documents while improving the detection of query intent.
-----------

**Why have you chosen this particular project?**

For one, this project involves application of the academic research, something I relish. Besides, integration of WordNet in Xapian has potential to extend it beyond conventional use cases and improve upon existing ones. A main problem with the current search engines is the large volume of documents extracted as a result of broad, general queries, and the lack of output produced to specfic, narrow questions. Current method for matching terms directly with document index not takes the sense diversity of words into account. I am improving Xapian in this area.

**Who will benefit from your project and in what ways?**

Out of seven billion people only five percent of them speak english natively. Moreover, there are only one billion total english speakers while more than 50 percent web content is in english language. This creates a language barrier for rest six billions to access majority of information as their vocabulary is not evolved enough to frame their query efffectively. 

WordNet integration will facilitate such people by adding more flexibility to interpretation of certain queries in particular. 

Besides above, the most benefitted usecases:

* Search pool containing highly heterogenous information or,
* The user is not well familier with the resource jargon

These constitute majority of the userbase. This project will work to quantify intent of queries and judge relevance of a document by improving upon existing term match methodology using WordNet semantics data.


Source: https://en.wikipedia.org/wiki/Global_Internet_usage
.. For example, think about the likely user-base, what they currently have to
.. do and how your project will improve things for them.


Project Details
---------------

.. Please go into plenty of detail in this section.

**Describe any existing work and concepts on which your project is based.**

FILLME

**Do you have any preliminary findings or results which suggest that your
approach is possible and likely to succeed?**

FILLME

**What other approaches to have your considered, and why did you reject those in
favour of your chosen approach?**

FILLME

**Please note any uncertainties or aspects which depend on further research or
investigation.**

FILLME

**How useful will your results be when not everything works out exactly as
planned?**

FILLME

Project Timeline
----------------

.. We want you to think about the order you will work on your project, and
.. how long you think each part will take.  The parts should be AT MOST a
.. week long, or else you won't be able to realistically judge how long
.. they might take.  Even a week is too long really.  Try to break larger
.. tasks down into sub-tasks.
.. 
.. The timeline helps both you and us to know what you should do next, and how
.. on track you are.  Your plan certainly isn't set in stone - as you work on
.. your project, it may become clear that it is better to work on aspects in a
.. different order, or you may some things take longer than expected, and the
.. scope of the project may need to be adjusted.  If you think that's the
.. case during the project, it's better to talk to us about it sooner rather
.. than later.
.. 
.. You should strive to break your project down into a series of stages each of
.. which is in turn divided into the implementation, testing, and documenting of
.. a part of your project. What we're ideally looking for is for each stage to
.. be completed and merged in turn, so that it can be included in a future
.. release of Xapian. Even if you don't manage to achieve everything you
.. planned to, the stages you do complete are more likely to be useful if
.. you've structured your project that way. It also allows us to reliably
.. determine your progress, and should be more satisfying for you - you'll be
.. able to see that you've achieved something useful much sooner!
.. 
.. Look at the dates in the timeline:
.. https://summerofcode.withgoogle.com/how-it-works/
.. 
.. There are about 3 weeks of "community bonding" after accepted students are
.. announced.  During this time you should aim to complete any further research
.. or other issues which need to be done before you can start coding, and to
.. continue to get familiar with the code you'll be working on.  Your mentors
.. are there to help you with this.  We realise that many students have classes
.. and/or exams in this time, so we certainly aren't expecting full time work
.. on your project, but you should aim to complete preliminary work such that
.. you can actually start coding at the start of the coding period.
.. 
.. The coding period is broken into three blocks of about 4 weeks each, with
.. an evaluation after each block.  The evaluations are to help keep you on
.. track, and consist of brief evaluation forms sent to GSoC by both the
.. student and the mentor, and a chance to explicitly review how your project
.. is going with Xapian mentors.
.. 
.. If you will have other commitments during the project time (for example,
.. any university classes or exams, vacations, etc), make sure you include them
.. in your project timeline.

FILLME

Previous Discussion of your Project
-----------------------------------

.. If you have discussed your project on our mailing lists please provide a
.. link to the discussion in the list archives.  If you've discussed it on
.. IRC, please say so (and the IRC handle you used if not the one given
.. above).

I've discussed it exclusively on IRC.

Licensing of your contributions to Xapian
-----------------------------------------

**Do you agree to dual-license all your contributions to Xapian under the GNU
GPL version 2 and all later versions, and the MIT/X licence?**

For the avoidance of doubt this includes all contributions to our wiki, mailing
lists and documentation, including anything you write in your project's wiki
pages.

Yes, I'm glad to do so.

.. For more details, including the rationale for this with respect to code,
.. please see the "Licensing of patches" section in the "HACKING" document:
.. https://trac.xapian.org/browser/git/xapian-core/HACKING#L1376

Use of Existing Code
--------------------

**If you already know about existing code you plan to incorporate or libraries
you plan to use, please give details.**

FILLME

.. Code reuse is often a desirable thing, but we need to have a clear
.. provenance for the code in our repository, and to ensure any dependencies
.. don't have conflicting licenses.  So if you plan to use or end up using code
.. which you didn't write yourself as part of the project, it is very important
.. to clearly identify that code (and keep existing licensing and copyright
.. details intact), and to check with the mentors that it is OK to use.
