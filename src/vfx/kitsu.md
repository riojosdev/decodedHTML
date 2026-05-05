# Kitsu

We are going to setup Kitsu. A collaboration platform for animation, VFx, Games. 

Our objective is to use Kitsu to be able to better manage and work with my past live broadcasts. Currently the workflow to gather the interesting moments are too much time consuming and disorganised and is hard to keep track of the output we need to have. Let's setup Kitsu to better manage this workflow.

## Zou
Zou is the Kitsu API. It allows you to store and manage your production data. 

### Installing Docker
* postgres
* redis
* meilisearch

The documentation explained the process for Linux environment, as we are using windows we had to install virtualenvwrapper for windows by running `pip instal virtualenvwrapper-win`, instead of the linux one i.e. `pip install virtualenvwrapper`

# We skipped the setting of environment variables

We created a virtual env in our windows user home directory, inside the folder Envs

### we initialized the database and migrated it with values, predefined by zou installation itself.

---

## Ran the Docker Kitsu Container
We got it running

## Learning and designing our own studio workflow
### Our specific purpose
#### Objective
Make an IG reel (entertaining)
Make a Youtube video (informative)
[optional] - Make a blog based on the youtube video (informative)

#### Raw assets
Past broadcasts

#### Assets
Clips of the past broadcasts

#### Tasks for assets
Organize the clips according to the engagement and information it has/provides

---


### We made our production 

### We made a sequence 

### We made a shot

#### Shot has individual tasks that needs to be done to be ready to be part of the sequence

---

### The creative director says this is a portion we need to have
* A shot is defined inside Kitsu, with task to clip/split/trim it

The best way to do this is using EDL (Edit decision list). Whose sole purpose is to be used for this specific purpose, i.e to represent the clips that needs to be edited. EDL is a list of timestamps that lists the edits that needs to happen for a particular clip portion.

AAF is a modern advanced EDL. 

---

### OpenTimelineIO


---

### XML vs EDL vs AAF vs OTIO
* EDL (Edit Decision List) is the most basic format to represent timeline information. It can be read by humans easily. Only the very basic information about the edits are tracked in an EDL file.
* AAF (Advanced Authoring Format) is a format that represents timeline information and the edits similar to EDL, but with more metadata about the timeline. Which is developed alongside Microsoft. It is saved in binary.
* XML is easier to read by humans but not by systems that are not Mac based. It is saved in hexadecimal. It also supports more metadata.
* OTIO (OpenTimelineIO) is represented in JSON format. Also supporting more metadata about the effects and layers.


---

### Initial Workflow Prototype Detail
EDL -> Kitsu Shots -> Tasks (READY -> Fetch Shot using OpenTimelineIO; WIP -> Use in NLE softwares)


---

### Sample EDL file into Kitsu
our initial edl and otio files was not able to be imported.
But we were able to import CSV files

---
---

shots
sequence
episode
edits

---

Episode
|
L* edits
    |
    L* 

---

shots -> example, if `storyboard` task status is not done, it means it dont have a place in the render, and it is being blocked from graduating to receive the tasks that comes after `storyboard`
         once the storyboard task is marked done, then other tasks can be worked on it. 
         in the end, when all the tasks are done, it can be compiled into the next stage, whether that be arranging it into the final sequence or an edit.

## How is this useful..?
We dont need to always load up an entire sequence, ie, a collection of multiple individual shots arranged in the timeline. just to make a small edit for a part of it.
Focus can be given to individual shots, and modify to improve the experience of it.

## 

Do not think about
* doing all the tasks for every shot. Only after the necessary prerequisite tasks for a particular shot is completed, you should attempt to further try to complete all the tasks it needs, for the shot to be graduated into the final production














## Resources
* [Opensource Assets by Netflix](https://opencontent.netflix.com/)
* [The Story Behind ‘Meridian’: Why Netflix Is Helping Competitors With Content and Code (EXCLUSIVE)](https://variety.com/2016/digital/news/netflix-meridian-imf-tools-open-source-1201859416/)
* [XML, AAF, EDL, WTF?](https://postperspective.com/xml-aaf-edl-wtf/)
