---
layout: post
title:  Techniques for teaching fully online
date:   2021-05-14 11:47:00
description: My takeaways from this year
---

I taught two fully online undergraduate classes this semester: *Data and the Art of Policy and Planning* (31 students), and *Urban Infrastructure* (14 students), and one last semester: *Introduction to Urban Analytics*. The two this semester were taught synchronously online through Zoom, and the one last semester was taught as a combination of synchronous/asynchronous classes online through Zoom. I am still waiting on my student teaching evaluations this semester, but so far, I have received very good feedback from my students. Below are some strategies I compiled:

## Online Small-Group Engagement
Making connections with peers -- for both making college friends, and also for engaging with people of different backgrounds -- is an important part of college. With everything online, there were virtually (haha) no opportunities for the serendipitous interactions that allow people who normally would not associate with each other to do so. For this reason, I made it a priority for my students to come together in small groups to talk in my classes.

I found that student groups of about 5-6 students worked the best (minimizing chances of having all quiet students, and yet still not getting too big for people to just chime in). These would be assigned "randomly" using the Zoom breakout room feature, though, I did start to notice that this feature does *not* seem to be random -- I think it is based on the the order in which people join the Zoom meeting.

I pre-prepare a Google doc for each group, which includes the questions that they should discuss together, and any relevant background information they need to refer to. This is an example of

<div class="row">
    <div class="col">
        <img class="img-fluid rounded z-depth-1" src="{{ site.baseurl }}/assets/img/teaching_google_doc.png" width="500">
    </div>
</div>
<div class="caption">
    An example of the small group Google Doc that I prepare beforehand for each group. Students fill in the document as they discuss the questions
</div>

**Some ideas**:
- Let students come up with discussion questions (as part of their grade for the semester)
- Have students come up with ice breakers to be included in the discussion sheet -- I was worried they would think this lame, but it seems they liked it! It helps them bond with each other and have a good time in class.
- Skits, role-playing, and group reading exercises
- I use the names in the group documents (which the students fill in themselves) to take attendance
- Make another Google doc, that includes the links to each of the groups, once assigned by Zoom breakout rooms feature.

Looks like this, where each Group # includes a hyperlink.

## Provide multiple entry points to access course content
Some students find being fully online difficult to keep concentrated on the class content. This is why it is especially important to provide multiple entry points to the material. That way, if a student finds it particularly to concentrate on synchronous online lectures, they may be able to access similar content through the readings, through just looking through the slides. A lot of these tips are applicable even when doing in-person teaching.

- Assigned readings (journal articles, white papers, etc)
- Course "textbook", basically my lecture notes, written in a colloquial style from me to them.
- Slides
- Lectures (do not assume that students have done the reading -- summarizing the assigned readings shows them what the important content/main ideas of the readings were. Showing them the connections between the assigned reading and the course themes shows them how to make connections)
- Recordings of lectures

## For technical content, prerecorded lectures tended to be preferred
I offered my *Intro to Urban Analytics* class in a hybrid synchronous-asynchronous format. I prerecorded all the technical content (learning specific functions in spreadsheet software, learning commands in Python, etc), so that students could follow along at their own pace. However, I also had once-a-week, 50 minute synchronous class meeting times to have students discuss the social context and implications of the datasets that we were analyzing. This was meant to have them realize the relevance of the work they were doing, build relationships, and understand that there is a lot of subjectivity in how data can be incorporated into urban policy, planning, and decision-making.


## For Python coding module, using JupyterHub was essential
Even in-person, installing the correct version of Python and required packages we used for my *Intro to Urban Analytics* class was difficult. Some students didn't have proper laptops (they were using tablets or chromebooks). Others' software resulted in conflicts in software versions. Others did not understand the importance of keeping code and data files organized into some directory hierarchy (they just saved everything in the 'Downloads' folder), and later could not reference the correct files. Solving these kinds of issues took of the vast majority of the time I was spending with individual students when teaching in-person.

After transitioning to all-online courses in the fall, it would clearly become impossible to do this kind of troubleshooting with students. Instead, we relied on a shared [JupyterHub](https://jupyterhub.readthedocs.io/en/stable/) running on my server on campus, which students could access simply through their web browsers and Virginia Tech's Single Sign-On authentication system. This meant that all student would be running on the same hardware, all data files would be saved in the same locations, and they could access all of it, and edit/run their own Jupyter notebooks using my remote server's kernel. Each student had their own personal directories and files. When they were finished coding in their own notebooks, they could then download the notebook and turn it on Canvas.
