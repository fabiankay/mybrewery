---
toc: true
layout: post
description: My learning journey
categories: [reflection]
title: My learning journey
---

# My learning journey
While planning the mybrewery application and working on our Frunch Infinity project, I learned a lot about developing software in teams. So far my experience was limited to projects as a single developer or product lead without responsibilities towards development practices. Therefore, the experience of working in a team or planning software to be developed by a team was very valueable. My key learnings can be summarized in two main topics, namely planning software for agile projects and test-driven development under time pressure or in larger teams.

## Agile Development

![]({{ site.baseurl }}/images/agile_meme.png "Agile Meme")

There might be more agile practices and methodologies in place than there are developers on the planet. I've read and learned a lot over the past couple of years. I've also seen a lot of different development projects. Yet, none of the was the same and all of them claimed to be agile or even SCRUM in one way or the other. To me it seems like every project tailors different concepts and methodologies to suit their needs. This seems ok and might work well for everyone but on the other hand it makes communication much more difficult. By saying "agile" I am now more aware that everyone might see it a little bit different. Therefore, it makes complete sense to outline and define development practices, standards and other artifacts in advance so everyone is on the same page. This helps the team to work efficiently and focus on results rather than processes (as stated in the agile manifesto "individuals and interactions over processes and tools").

While planning mybrewery I had doubts wether overthinking parts of the software is still in line with agile principles. I started documenting and designing the software without writing a single line of code to test its implementation. As already mentioned within the lecture, coding is only a small fraction of software development. Yet, overthinking the software might lead to a waste of resources when the plan fails or requirements change. Agile principles argue for delivering working software over documentation. I feel like it is hard to balance both aspects since I also see the need for documentation and planning. For example, the class diagram helped me thinking through different options of implementing different ingredients. If I coded my first thought, I would have found myself refactoring the code already during the second iteration. In this case, carefully planning the structure in advance saved a lot of time.

I come to the conclusion that high level planning helps a lot to get a first idea of what's coming. On the other hand, overplanning things is not helpful either. The critical step is to find the right time to start implementing. For my brewery I am at that point right now. I think a have a good plan to start the first iteration and implement an MVP. It is now the task to reduce the planning to an implementable set of requirements.

## Testing

![]({{ site.baseurl }}/images/testing_meme.jpg "Testing Meme")

Another key learning from the projects described is related to test-driven development. The idea sounds great and I haven't worked with test-driven development a lot. I remember the times when we tried to implement it in our company - we faced similar issues to what I experienced in our projects. When time becomes a topic, tests come last and production code is the priority. Moreover, during development it is also hard to keep tests up-to-date and requirements change over time.

In those cases I understand the priorities. On the other hand, when shipping code to production that is untested (at least in terms of code test coverage), there is this strange feeling if everything unchanged is still working. This feeling was present in our Frunch Infinity project. We had an okay test coverage. Yet, some parts of the software were not covered by tests. After every push there was a short feeling of uncertainty. 

Having 100% test coverage seems unreal to me. But having the most important parts of the software covered establishes a comfortable feeling.

At the beginning of the course I felt like I had some experience with software development. But after doing both projects I quickly realized that practicing on real-life projects always leads to new learnings.