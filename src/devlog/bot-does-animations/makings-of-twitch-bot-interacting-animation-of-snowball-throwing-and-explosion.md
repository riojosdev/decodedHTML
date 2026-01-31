# Makings of Twitch Bot Interactions of throwing a snowball with explosion diffusion animation

## Abstract
I recently started build a Twitch bot. I wanted to make it to bring in some interactive stuff for the viewers to use, using specific commands. I was insipired to do a snowball throwing animation from another streamer friend. I started building it using vanilla JS. Following the Twitch Docs. I got the Bot to login to Twitch.

At the very start itself, I wasn't sure of the best structure I should be following to architect my Twitch Bot Application. But twitch itself had a sample bot as a part of their quick start guide/documentation. It was enough to get started on getting to know their APIs. Once I came across it, I read through the code, to know, if the sample would suit my own purpose. 

I had previously built a Bot for Meta's Threads App, which could create a threads post, schedule it, and even attach media. I went a little overboard and also added the ability to post a threads post using SMS, leveraging the Twilio's API. Everything was architected in such a way that I was able to make quick changes later on, if needed. This very structure also came to my help.

Reading the code is one of exciting activity developers love to do, learning about the structure of how a system is built and how it can be accessed. It makes us visualize how we can further improve and structure it according to the specific purposes we require. Initially I tried to look at if there were any libraries I had less knowledge on how it worked also touching up my knowledge on some previous known libraries I used in other projects. 

## Webhook
### The example chat bot were built as an example - Do I use the very same code or architect one for the specific requirement I have
Getting to know the how a code works just by reading through it, I had my suspiciouns on how it would be a bit error-prone. And I would probably be trying to fix all those bugs that come up later on, which would mean I've to go back to the example chatbot again and again. So, I decided to try the example chatbot first, run it, then expand on it features by modifying different parts. I could then later come up with a better structure, once I know what all features and workflow I need to be using. Refactor is always done, once something gets too complicated. It makes you consider certain ways of doing stuff, to of making it better, easier and access/modifiable faster.

> Also, there's a point I do think about this. If only I could create the application without actually testing out the sample code. And I move on to find the best possible architecture. And this puts me in a state of being overwhelmed by lots of different ways other people have architected and their design decisions. It's overwhelming and makes me lose track of my actual goals.

* Copy pasted the entire sample bot code from twitch github repo. Into local env
* npm install the packages that was used in that particular code file.
* Since i was streaming, I made sure to place the secrets keys in the .env file.
* Modified the web page output that would've shown the access token on stream, to show nothing, but kept the username to be displayed
* I only had the client id and client secret from twitch api dashboard. I wanted to know what the session secret was. (spoiler: it's a random bunch of characters you can define yourself, to keep track of the current session you are in, something to think about when you are the client.

> Since I was streaming, I was getting a bit slow, when it came to handling the secret keys appropriate, without doxxing myself on my livestream. One of the concerns I had. I was reading and undertanding the docs really carefully, so I dont take a mistep.

### What was the first thing I wanted to do. There were a lot of APIs to work with, what do I actually need
As a basic chatbot, the code already provided showed way to send a message and listen to specific messages and do some kind of operations when triggered. Initially this was a webhook chat application.

Initially the chatbot was using twitch's webhook apis. Which was a bit confusing, as I didn't wasn't familiar with passportjs library. And as I wanted to just have a prototype ready quickly (still not ready - at the time of writing this post) I skipped the webhook entirely, since using curl and testing out the commands was easier in order to know how the entire authentication process of twitch worked. 

During the development of the webhook chatbot, I was confused on multiple guides on helping with the setting up of the chatbot. I came across the websocket chatbot page too, and the authentication of that and the webhook ones, made me again a bit confused. Is this just me or is this how y'all developers who worked on twitch api felt like. This was probably because I had multiple tabs open of the twitch docs, of different information needed to set up a chatbot. I had to clean up the tabs to keep me grounded on my current actions.

Here's the clip of me running the sample Bot code, I haven't provided the session secret and callback url. I wanted to know the errors that would pop up, so I could handle it properly, if I was to stream the entire development of it. Again didn't want the error messages to reveal some secret keys later. There was a choice here, in which I could just provide all the secrets and let it run, but that would've made me less confident in developing the bot live, as I needed to assume the any error during authentication would reveal a part of the auth secrets, which would dox my bot.

### Issue: What is actually the session secret required when running the webhook bot
So, the session secret is a string which can be anything I am able to define by my own. I could use like a UUID and make it more unique everysingle time, but for my purpose it was not really needed, I used a bunch of random characters which I made by hitting random keys on my keyboard without looking. I first thought it was something I needed to get from twitch itself. But, no. It's just a random character string used to track the current session that got authenticated, which is useful, when the bot need to log back in. Or we would need to login every single time when the token gets expired.

> What the session needs to be is not talked on the twitch docs, probably for the developer who was going to use the API, knows how it should've been. Consider if the docs said it just needed to be random chars, for the dev to keep relogin. Defining it and presenting it in such a way in the docs would've made the developer to not really put in the effort to secure the application. This way the developer would research different ways a session secret should be constructed. Or it would've been easier to use another's session and that would be a disaster.

> #### How did you not dox your bot secret keys when developing a Bot

### Issue: Data not being shown on page
Once I provided the right session secret and the callback url. I was able to get to the handlebars defined webpage. But the data used to represent in the handlebars template were not showing. I just wasn't parsing the data to JSON when being retrieved from twitch api. Which is one of the most common errors often faced during web development. And it completely skipped my mind, wasted some time around it, but nevertheless, the data is now being retrieved and rendered on the webpage. Showing the 

### Issue: Providing the correct scope grant types
So, when I was developing, providing the scopes for reading and writing in chat was not being able to parse correctly, I was missing something here. The scopes being serialized and parsed using passportjs required a different format. Still haven't fixed that, but I found I could do this in curl. Which means I just have to go through passportjs docs inorder to fix it. (IF IM READING THIS, FIX THIS, THIS A TODO).

The authentication workflow I was able to access through curl. And once I got that done. I wanted to re-prioritize to make the initial prototype to get the snowball animation test bot. Thinking about it, I want to get the ability to listen to chat messages and respond to it. And making the webhook app, was a bit of a struggle to setup, I wanted make sure I was passing in the correct way, using curl. It took me a few tries, tring different combinations of unicode character representation (mainly it was because of the underscore).

Once I got to know how to get the token for the bot using Curl. Websockets was the only option to actually listen to the chat messages, using the webhook means, we had to use the webpage whenever we wanted to make a certain action by the bot. I wanted the Bot to be constantly listening to the chat, so it could respond and make it as interactive as possible. So Websockets..

## Websockets
Websockets is the way to constantly listen to the chat. And each actions that needs to be taken place could be done as an side effect
The code for the websocket chat bot was taken from the examples by Twitch docs. Authenticating the
### Issue: Is the broadcaster id and user id the same
When I was going through the Twitch docs for testing out the different endpoints, and to setup my websocket connection. The user id and broadcaster id was required to make an API call. I had to look around more to figure out if both were the same. It turns out it is.

### 
The initial webhook endpoints are used to get the access tokens for the bot to function. I had trouble providing the correct way to request the required scopes that was need to listen to Twitch chat by the websocket part of the Bot. The required scope mentioned in the docs was `user:read:chat`, and it was supposed to be passed in the url of the request. In the sample bot code, it used passportjs. Which had a different way to represent the `:` character. This caused a bit of a problem. The provided scope in the sample code showed only `user:read` which was written in the sample code as `user_read`, doing the same for `user:read:chat` and `user:write:chat` just bought up errors from the bot because it was not the one recognised by Twitch API.

### Issue: Twitch uses different types of token for different purposes, I was using the wrong token (webhook) for the websocket app
### Issue: The token I received from the Twitch authentication workflow, responds back with invalid token
Twitch has multiple authentication workflow for retrieving different token types. Currently they list 3 types of token. A user access token, Id token, App access token. You can [refer the docs which has documented them more detailed](https://dev.twitch.tv/docs/authentication#authentication-flows). It skipped my eyes when I was developing the bot.
> Apparently going back to the documentation, I see it being said at the very start of the authentication docs. 

### Once I got the websocket twitch bot client reading and writing to chat, the next step was to integrate OBS, so I chat could control specific OBS functions I make
The very first thing I did was try to find out what all libraries would help in controlling OBS. While I looking into the libraries I also found multiple other projects that were using the OBS library. Which I had to explore to get more inspired and have a vision on what all I could achieve with it.

#### A todo i still have to do, discordjs guide had a wonderful architecture, which had separate file for each command that was available

### I needed both the OBS websocket library and the OBS API Library. 
The websocket OBS library was used to connect with OBS. And the API library for interacting with OBS.
