# Portfolio Redesigned using NEXT.JS with TailwindCSS, ChakraUI & a Morphing Gradient Background

<img src="./../images/riojos-portfolio-home-webpage-redesign.png" id="meta_imgz">

So, just wanted to prepare a devlog about my redesign of my portfolio website.

<p id="meta_descriptionz">Here we go into the behind scenes of how I redesigned my web-app development & graphic design freelance portfolio webpage riojos.in, built using NEXT.JS, TailwindCSS, ChakraUI & a Morphing Gradient Background by WeCoded's Youtube Tutorial. I deployed the final webpage on Vercel! Let's go into more depth on the development.</p>

My decision for the redesign started when I wanted a page for to showcase my projects. My previous design I had just a UI with some simple HTML div elements, CSS & [GSAP](https://gsap.com/) to animate a section where latest updates would be shown. Unfortunately that component went under developed as I didn't have any cool/fully finished projects to show on my portfolio. I thought to show some blogs I written here. But that would've meant I would be skipping my opportunity to develop some projects to showcase my skills. So particpated in a hackathon to get that pressure to build & ship fast. Some developers work well under pressure, like me. Not good behaviour, I know. But I usually get distracted. In this era aren't we all living in the attention driven economy. And we all do experience ADHD from time to time I guess. Some cope well better than others.

The plan to improve heavily on the frontend design & development was to promote my NPM library Jaggery.

## The Frontend Components
### NavBar
<img src="./../images/navbar-component-from-jaggery-library-transparent-background-with-glowing-link-on-hover.png" alt="">

The NavBar component is primarily built to support to be imported into a create-react-app project. I built this component and published it onto my [NPM Jaggery Library](https://www.npmjs.com/package/jaggery). I had some issues on getting it directly imported into the NextJS portfolio project. But as I wanted to implement the portfolio first. I tried extracting the component and implementing it directly onto the NEXT.js project.

### Morphing Gradient Background - by WeCoded's YouTube Tutorial
The main attractiveness to my portfolio is from this [background interactive Morphing Gradient animation tutorial by WeCoded's YouTube Channel](https://www.youtube.com/watch?v=Ml-B-W91gtw). On his tutorial I learned about how you can apply shaders using HTML SVG elements. I immediately got hooked on it. And since it looked really well on my portfolio, I want to do more research on it & also share with you guys. So my plan is to prepare a course on XR (AR/VR/MR) & to start with the HTML SVG element. So, will be soon posting a link about it. Make sure to follow me on any socials you can find on my portfolio page to stay updated on when it would be available.

### Scroll Progress Circular Tracker
<img src="./../images/scroll-circular-progress-tracker-with-transparent-background.png">

The idea for a scroll tracker was inspired by my friend's blog page. I used [ChakraUI](https://v2.chakra-ui.com/) to implement the progress track design. Added a custom CSS on top of ChakraUI's component, as I had some issues in getting my desired CSS Style to be applied on the component.

### Card Container Components
<img src="./../images/transparent-designed-card-layout-by-chakraui-and-container-component-using-tailwindcss.png">

The different card container components are used to represent a section. Which was built & stylized using [TailwindCSS](https://tailwindcss.com/) & [ChakraUI](https://v2.chakra-ui.com/). Additional CSS styling were added on top of ChakraUI to math the whole theme of the Portfolio page.

## The Pages
### About
The about page has a bried description about my journey into freelancing. How I started programming. What are my main motivations, lessons & things like that. Do give a read to get to know more about me.

### Projects
My own ideas that I tried to get my hands dirty. It shows what I really would do. And what all I have learned. The opportunities of each project is different. It gives you an idea, of what is possible with me included in your team. And what my project is able to do. Don't let the projects go unseen, as they have immense potential to create a big dent in this tiny blue planet. But to take it forward, you would need to love dirt.

### Services
The most services requested from me. These are not my only capablities, I can provide, but since these are the most often contacted me. I added it a place where you can reach out to me easily. Describing more would just mean, I would be forcing my ideas on to you. We all live in & come from different dirt on this planet, no?

## Server Actions & Middlewares
Postgres Storage on Vercel powered by NeonDB
I used PostgreSQL as the database by following the [Vercel Postgres Storage quickstart](https://vercel.com/docs/storage/vercel-postgres/sdk). Vercel let me have an easy to use dashboard to be able to monitor postgres data. I used it for the enquiry form on my portfolio.

## NextJS Redirect
The NEXT.js config file had an option to make a redirect towards an address. I wanted to use it for having an fancy human readable url format, rather than something that was too long to even be visible in the browser address bar. The shorter URLs makes it more memorable. So loved that NEXT.js offered it directly on it's config.

But before getting to know the option of redirect from the NEXT.js config, I tried implementing a server action to redirect the page. So that I may be able to display a loading animation that the user was being redirected towards an external link. If I could've been able to implement that, I could've used the meta tags and log the visit direct on my NEXT.js portfolio.

I don't know if this is not possible or not, but the data couldn't be SELECTed and received on the client component. The redirect function was defined in the client component inside an useEffect hook. So I wanted my data to reach the function call inside useEffect. But the SQL query as it is always async it returned a promise. And it was not possible to get the value of the promise. I was hacking my mights off on this.
