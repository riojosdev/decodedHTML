# South Indian Malayalam Film ANOMIE Uses Sound Particles For Their Sound Production

We were looking at file samples. Learning about how the EDL format is. We discovered the file assests that are being used in a film production.

We were thinking about creating an adapter for OpenTimelineIO. To be able to fetch Youtube videos (our past livestreams) and fill in the necessary metadata. And maybe use FFMPEG to do slicing edits, to be more resource efficient. The workflow I plan would be like create OTIO (EDL) list of clips needed. Provide it to Kitsu. Then when we are ready to work on a shot. Change the task type to `Ready`. Which would fetch the file using Youtube API, which is then handed over to the FFMPEG library to slice into clips and save locally in the edit folder.

We were looking at file format of OTIO. How studios are able to use it. We are using EDL (on progress). And actual Studios used XML. 

The actual studio asset files was discovered on Raven (OTIO viewer) app's Github repository. Which provided the resources by Netflix (Open Assets)

I looked at different assets. But also focused on ADM. Which was the format that contained the metadata for sounds.

I wanted to know, how the recent news I heard. About how a south indian film Anomie, might have used it. They talked about Sound Particles.

I visited the Sound Particles website and did a quick breakdown on how the system worked. In order for our Kitsu pipeline to be able to suppor sound related tasks.

TLDR: They had developed an application for Sound Production Professionals to work with Sound samples as seamlessly as possible. Their software guaranteed good UX and accessibility.

I felt excitged to watch Anomie. To evaluate & experience how a South Indian Malayalam film crea did the sound production.

If you're working in sound production or a audio/sound enthusiast. I definitely recommend you to watch it in theaters and experience how a professional film crew are being benefited from using Sound Particles, to get you immersed in their creative production.

I am looking forward to get immersed & inspired in ordr to architect our own Kitsu pipeline with a realistic ADM format.
