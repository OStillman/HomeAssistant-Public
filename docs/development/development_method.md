# My Development Methodology
I've gone through quite a few different small development projects for my own personal use and fairly quickly I realised it needs a proper plan to ensure a smooth flow.

So, using pre-existing methods, I created my own methodology!

## The ODAC Development Methodology
3 Phases:

- Phase 1: Proof Of Concept
- Phase 2: Use and Improve
- Phase 3: Add the Smarts
- Phase 4: Post-Development

Tools:

- Trello Kanban Board - Not Started, In Progress, Testing, Complete
- Github - Phase 2 onwards for issue tracking & resolving

### Phase 1: Proof Of Concept
**What?** A Phase used to develop the initial concept, test out the idea and see if it'll be useful

**How does is it play out?** Generally this is the stage I'll jot down ideas, create my Kanban Board and start developing from there. Almost as if I'm the Customer.

### Phase 2: Use and Improve
**What?** Now the Proof of Concept is built and functioning, let's use the project and see if it's actually useful - referring to my mission statement! You could call this an extreme version of Hypercare

**How does it play out?** Small, quick iterations of development. Usually, I'll find I've missed a key aspect (e.g. in how the UI is built, the logic etc.) and I'll re-plan and develop

**Where do you go from here?**
There are multiple routes:

- Phase 2 Repeat - Add new feature and use it. Is it enough? Does it work as needed? etc.
- Return to Phase 1 - Current build is not functional and/or misses out on a BIG feature, so back to the drawing board for a re-build
- Move onto Phase 3 - Project works, it's been used and improved as much as required
- Remove Project: Project is not needed, so development halts

### Phase 3: Add the Smarts
**What?** Smarts mean integrations into other systems, hardware etc. For example let's predict when the user may want certain information and send notifications at the time it'll most likely be useful for them!

**How does it play out?** Fairly slowly, the project is mature at this point and we know things work as they need to. It's likely Phase 2 will be returned to

**Where do you go from here?**
There are againn multiple routes:

- Return to Phase 2: You've found a big feature that needs implementing, using and improving
- Move to Phase 4 - Either, Smarts are not required, or Smarts have been added so Phase 4 can now be moved into

### Phase 4: Post-Development
**What?** Almost like the LTS (Long Term Support) Phase of large developnment projects. Some bug fixing, some enhancements but largely the project is in a working state

**How does it play out?** Little movement will occur, development will slow or even halt. Bugs tracked and some resolved. Phase 1 or 2 can be returned too depending out outcomes

**Where do you go from here?**
Less Options, but still exist:

- No Movement: Project works, is functional and satisfactory. If it ain't broke...
- Return to Phase 1: Project requires large overhaul e.g. Website to App. Proof of concept required
- Return to Phase 2: Project requires new feature which will require hypercare on implementation
- Return to Phase 3: New Smarts are Possible and Useful to implement


### Case Study: ODAC Shows
ODAC shows is the main Project I've worked on that's made full use of this Methodology. It's played out as below:

- Phase 1: Built fairly quickly, list of shows we were watching
- Phase 2: Quickly Realised the following:
    - Simply adding a list of shows does not work
    - A Daily "what's on" of live TV would be far more useful
- Return to Phase 1: Live TV and On Demand TV MUST be treated seperately:
    - Live TV is on more than once a week, we need to rely on TV Listings to get when a show is on
    - On Demand can be kept as a list in categories as that works well
- Phase 2: Improve TV Listing Use
    - Formatting is not the same throughout all TV Channels
    - Fix issues where Series number is not always presented
    - Fix other issues with Series Numbers and Episode Numbers
- Phase 3: Notifications
- Phase 4:
    - New Items are being planned including visible screen, auto channel changing but these are future plans
- Phase 1: App Required
    - An App is now required to streamline the experience and create a fully-developed API seperated from Front-end logic
    - Proof of Concept of Native App Required - improve UI and ensure useful to others
    - Plus, name change to the current name ODACShows
    - Pull out of Main Pi_Webserver Repo to seperate Development Effort and Dependancies