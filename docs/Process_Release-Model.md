# Release model

**Release Dates**

Armbian runs "train" based releases. Whatever is ready to board the train, does so. Whatever isn't ready, has to wait for the next train. This enables us to have a predictable release cycles making it easy to plan. It also puts the responsibility on developers to make sure they have features ready on time. 

Armbian releases quarterly at the end of **February, May, August, November**. Offset is because we all know that nothing happens for half of December. At the beginning of a release cycle, we have a planning meeting and two weeks before the end of the release we freeze integration of new features.

**Release Cycle**

Releases last 3 months. Each release starts with a planning meeting. After planning, developers and development teams build their deliverable using whatever methods (scrum, kanban, waterfall, ... ) they want but shall commit their code frequently, leading up to the last 2 weeks. The project does not accept "dumps" of code at the end. Commit early and often on master. Two weeks before the release date, we halt feature integration and only allow bug fixes. At some point during those two weeks, we start the release candidate process. This process starts by pulling a branch off master that will become the release branch. That frees up master for development on the next release. On the release candidate branch we work on bug fixes, and choose "release candidate", RC, tags. The software at that tag is a candidate for release, and it is submitted to automated and manual tests on real hardware. If automated tests are passing, we can officially tag it as the release. If it doesn't, we enter another bug fix cycle and create a new release candidate. We iterate until we have a candidate that can be the formal release. Usually, this takes 2-3 cycles and 1-3 weeks of time.

Development epics, stories and bugs for each release are tracked through [Jira](https://armbian.atlassian.net/).

# Release Branching, Versioning and Tags

Branches in Armbian follow this convention: 

 - **Master branch (master):** Main development will happen on the master branch. This is the latest and greatest branch, but is always "stable" and "deployable". All tests always pass on this branch.
 - **Maintenance branch (support):** This is the long-term maintenance branch per release.
 - **Development branch (dev)**: This is a branch created for lengthy and/or involved feature development that could destabilize master.

Each Armbian release will have the following version format:

**Format:** `<major>.<minor>.<revision>`

`<major>` and `<minor>` version will be incremented at the end of the release cycles while `<revision>` is incremented for a fix (or set of fixes)

Tags are used in ad-hoc manner.

# Release Naming

 19.11 Kuza
 
 20.01 Muca
 
 20.05 Riba
 
 20.11 Zaba
 
