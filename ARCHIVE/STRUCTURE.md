# WIP

# DevConf Blurb
“I am not paying $40 to make an HTTP request.”

Sorry.

$75... and it’s only TCP. You’ve got to do the rest yourself.

This talk focuses on the journey of an engineering startup’s software team, how completely and utterly unprepared we were for the hardtech* engineering world, and how one’s values, stubbornness, and idiocy (deciding to go against 40 years of industry dogma) are, occasionally, the perfect recipe.

I will focus on the problems of closed-source vendor lock-in, and how zero community libraries, “license fee extortion,” limited proprietary tools, and pure frustration led my team and me (one web developer and two fresh graduates) to take a daring risk, and the rewards and horrors we faced along the way.

No tools, no libraries, and I sure hope you love Visual Studio 2016. But necessity is the mother of invention. This is how we built an entire library from scratch, leveraged a protocol in ways the vendor did not expect, and ultimately broke free from closed systems to use the tools and workflows we know and love.

This talk is for those of us who have had crazy ideas but struggled to find market fit or justification for them. It’s for those who don’t know where to start. The many false starts, and how they ultimately led to our success. I am incredibly proud of the work we’ve done and the challenges we’ve faced along the way.

And all of this was done in Cape Town - African solutions to solve African problems.

I will talk about why we did it, how we did it, how juniors can be the most powerful tool at your disposal, what we’ve learned, and how on earth I convinced management to agree to this. The talk will include light technical elements (design decisions, the complexities of PLC vs. PC systems), but will focus heavily on encouraging participants to trust their gut and recognise that our local talent is truly exceptional.

“Hardtech” is not meant to imply difficulty, just that when you physically bang your head against it, it bangs back.


### Takeaways (Audiance Blurb):
[x] Engineering Startup.
[x] Migration from Web Based to A single IoT Device.
[x] The Industrial Automation Industry (Costs, way things are done, Development Environemtns from Hardware Vendors)
[x] History, and how did we get here.
[x] Standerdization
[x] License This, License That.
[x] The Reality of 'Pay Per License', and the moment of "oh no, I know where this is going"
[x] What are we playing with?
[x] What where we expected to do?
[ ] Team Composition, and why this is important
[x] A one year journey
[x] How we managed to do this?
[x] What we managed to create
[x] HAL, and decoupled development
[x] Ok, but why? Why do we live in this world
[x] African Problems Need African Solutions
[x] What's Next?
[x] Outro (Talk Location, etc, etc)
# DevConf Blurb (Organizer)

### Takeaways (DevConf Blurb):
[x] Who I am?
[ ] Communities, Hardware Development, Splitting Time
[x] Industrial Automation, What is it?
[x] How Control Works
[ ] How hardware measures a value
[ ] Cadences of Development?
[x] Moving away from Real-Time Control
[x] MQTT, and finding a technology that works
[x] Management, and getting buy-in
[ ] Moving The Needle
[ ] How the sausage is made.
[x] Kruger Dunning Curve, and slef-imposed limitations (limited by the world you are aware of)
[x] Short Term Cost, Long Term gains (Internal skill development, a project to own).
[ ] Not all wins are felt, some are simply the abscense of a loss
[ ] Handling discomfort, self-doubt, anxiety, and nearly blowing everything up - Twice
[x] Indsutry Change, Open Sourcing, and the excitement of being ignorent (Junoirs)

# Scratch

Hindenberg, Duckenberg
What are we trying to do? Energy scarcity. African Problems, Modern world impact
You only appreciate it when it's gone.

The Point Of This Presentation
Take Risks, Solve Structural Community Problems

Summary
South African Company using old, outdated and closed off software.
The problem we are solving.
Frustrations, and serious issues involved
Breaking Free, how we did it, and what we plan to do
The benefits,
The problems,
Why is this not solved? why do we still need locked in manufactuers
Splitting Developers
Creating an Industry that is not accessible
Next steps (Fromo HYENA)

# Target Presentation Length: 30 Minutes
# Intro + Preamble (3 Minutes)
- Who I am
- Background
- FanFare

# Disclaimer
- I really appreicate the vendor we use
- No shade, or shame. This is the reality of the industry.

# Why we are all awesome.
- Why are we here?
- Well, we know this, but do we really?

# What do I do now?
- HYENA, Brief Overview of What we do (not how)
- My Team and I broke out of a closed source

# What do you mean... closed source?
- Description
- Where is the community?
- Don't ask reddit for advice.
- Well, why don't you just use open source?

# Welcome To The Industrial Automation Industry
- Some Background
- Conventions are rather Convenient
- What do we mean by real-time really?
- Industrial Control
- The Good, The Bad, and the Ugly
- Mention Cobol

# But surely, the closed-source is ok?
- No. Absolutely Not.
- This is not microsft Word.
- Insert Clippy meme

# Putting a Price on all of this
- Real Cost
- Lot of Upfront CapEx.. But if it's a one-off?

# But wait, there's more.
- Licenses,Licenses,Licenses
- The  privliedge of building an HMI/GUI
- All of this is dependent on ability of machine

# Why this makes sense?
- Industrial Automation  projects cost millions of USD, what's a few 100K going to you?
- No problem with paying for software
- But I will NOT pay for the 'privliedge' of making a web request.
- The 'community' seems to embrace this.
- This is where the reality set in

# Walled Garden
- Explain what it is
- Explain costs associated
- Explain non-costy-costs asasociated
- This mental philosophy encourages holding your cards close

# Effectively A Monopoly
- We're not going to move away
- But that means... we will never move away, and we're just getting more indebted
- Developer Experience does not exist
- Documentation is sometimes a joke
- AI Ain't going to help you due to lack of exposure

# How to break away
- One small step at a time, and that first step is Buy-in
- isolating what we could and could not replicate
- Put a price tag on it. Management likes this. Cost Sensitivity. We also had time on our hands
- We had a version 1 backup. Which allowed us to do hardware testing in parrallel
- Hardware Testing takes long, and there's a lot of lag time.
- Interim Connections

# How Long, and did it work
- Yes, exceptionally well

# So again. you guys are awesome.

# Not done yet,
- We're still dependent on a common PLC core.
- 40 years ago... this made sense, but now...
- This is not easy, but this needs to be done.
- There is work to be done to create an isolated PLC system
- Story for another time.

#  Question
