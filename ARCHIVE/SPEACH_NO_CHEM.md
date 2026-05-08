00:00 -    Good Morning Devconf! I'm exceptionally excited to be here. This is actually my first presentation
           On Home Soil!

00:00 -    I'm here to talk to you today about this rather strange situation. How on earth did we find ourselves
           In the rather procerious situation of having to pay $75 for the privliedge to make a TCP request.
           in todays world... quite simply? wtf?

00:00 -    So, without further pandering, let me tell you a story! But First. Who am I?
            <slide>
           My name is Warren Fletcher. I'm an electrical engineer who has spent a decade
           the wonderful webscale world. In the past I've spnt time at Amazon, Oracle, and
           Booking.com. I've been privledged enough to work in multiple domains from performance optimzation
           to a more busines focussed product-development, and finally to directly engaging with the customer.
           <slide>

02:00 -    In 2023, I returned from a 5 year stint in the Netherlands. While it was a life changing couple of years.
           I, quite frankly, missed the South Africa sun. I was starting to get a bit bored with web-scale products and
           wanted to get my hands a bit dirtier by getting back into the hardtech world of computer hardware, ellectronics,
           and control engineering. Subjects I had particularly enjoyed during my studies.

           <slide>
03:00 -    Fortuantely, that itch was soon scratched when I joined HYENA as a Systems Engineer. A startup on the
           sunny, albeith windy, beaches of Muzimberg in Cape Town. HYENA originated as a spin out form UCT.
           And we are a rather ambition group. Our main goal is to make the apparent science fiction world of Fuel Cells a reality.
           And we are doing just that, with a focus on the local African market and our rather special electrical and geographic limitations.

           We are a extremely diverse collection of university academics, seasoned chemical engineers, electrical engineers and software programmers.

           While I would love to spend my time today talking about the unique chemical, electrical, and mechanical properties
           involved with the usage of a Fuel cell. That will have to be for shelved in the intrest of time. But the executive summary, is that at HYENA, we
           <slide>
           are producing a diesel generator replacements that are quieter, more efficient, and less toxic to users and the environment. This, as per our name, all
           <slide showing render of PowerPod>
           based off of fuel-cell technology, and some tricky chemistry involving Hydrogen.
           <slide>

           As wide-spread Hydrogen is still scarce, we decided to use the fuels available today. In our African context, that is LPG. It is available throughout Africa,
           and yes, it is a hydrocarbon, so we're not fully green just yet, but watch this space.

           Specificaly, we use the hydro part of hydro carbon. Hydrogen

           To get this hydrogen off the LPG, we heat it up to around 800 degress celsius, before running it over a collection of catalyts. This hydrogen is then immediately consumed by our fuel-cell, and electricity as well as some water is produced.

04:00      For the remainder of this talk, we are going to focus specifically on the software and how one would even go around controlling these sort of hardware systems.

           What hardware/software is used,  how it is used, how different the two industries are culturally and technically, as well as what uphill battle we had.
           There is actually an entire industry related to jus this, known as Industrial Automation.

08:00 -    Industrial Automation.
           Industrial Automation is the intersection of hardware and software in a safety-critical environment with as little human involvement as possible.
           These projects very in size and complexity. But they are, above all, concerned with safety, longevity, and security by removing the human element.
           And humanity has been doing this for some time, and quite succefully. Projects ranging from
           <slide>
           Telescopes in South America
           <slide>
           Hydro-Electric Damns in China
           <slide>
           Electrical Generation in South Africa
           <slide>
           function the way they do because of the success of the Industrial Automationn Industry.

           Back Home in South Africa, we see it's use dominated by the mining, and agricultural sectors.

09:00 -    And this industry has been around for some time. Originally started in the late 1960s, it has only been growing since. Today, it's worth just under 270 Billion USD.
           and it all started with the introduction of a specilized independt computing unit called the Programmable Logic Controller. Often simply
           referred to as a PLC.

           The world, back then, was also a much simpler experience. These devices pretty much followed a simple cycle of
           <slide>
           read a sensor value, do some processing, and maybe make some sort
           of change via the adjustment of a valve or another actuator.

           This cyclic nature would continue indefintely, with the key requirement that at the end of every cycle, the device had finished it's processing.

           This cycle or sampling some these inputs written to hardware is repeated 100sto tens of thousands of times a second depending on the system  needs.
           Timing is a critical feaure, and any jitter in the start of these cycles can lead to system instability, and the endangerment of human life, inventory, or both.

           <slide>

           Not something you want to be playing around with on the first apple or windows machines. It would take another few decades for apple to become stable, and windows will soon be stable I'm told

            <slide>

           And PLCs did one hell of a great job. This industry exploded, and many hardware manufactuers saw the commerical opportunity in producing and supporting such devices, along with the associated hardware they need.

           <slide>
           In the software world, we are used to seeing products differentiated by languages and technology used. in this industiral automation world, we discriminate based on the vendor
           <slide>

12:00 -    What does this mean in a modern context
           The problem with specilized hardware is that vendors need to make hardware, and this hardware needs to be programmed. These vendors are in competition
           amongst each other, and have zero incentive to play along. And they don't. The programming environment one may use to program a Siemens PLC System cannot be used to program a Beckhoff System and vice versa.
           While these systems advertise that they speak the same languages. They also ship their IDEs with just enough vendor specific oddities that your code would require some degree of a rewrite at best if you moved over to their competitor.

           And while it may seem convenient that the software you use will run out-of-the-box.
           It also removed agency from the engineers who use them. They are, unwillingly, at the whims of the vendors.
           Eventually, over time, you end up with staff who only know a single vendors product.

           The thought of even using a competitor is a non-starter, as the upfront cost to company would be enourmous simply due to retraining costs alone.

           Great for the hardware vendor! They've got customers for life.

           We actualyl have a term for such a sitation. It's called a walled garden, and they are very prevalent in
           todays society. Weather by choice or by chance. Most fameously, Apple.

           Technically, not a monopoly. Just a significant amount of friction to desuade change.

15:00 -    So let's go back to a slightly younger version of myself.  Fresh off the boat of Web Scale, with it's exceptioanlly rich open-source ethos where comapanies
           often release their secret sauce for anyone and everyon to use.
           <slide>
           I was tasked with the slightly scary job of building the control system we were going to use to achive our fuel-cell dreams.
           One of our contractors supplied us with a PLC from a vendor they had been using for some time. Naturally, I went and started to read the documentation, and got around to isntalling their recommended IDE.
           Ofocurse, it runs only on windows. And it's also 32-bit for some other reason. Did you know that windows file paths are limited to 260 characters.

           Red Flags in retrospect, but our younger Warren thought it as a simple oddity. I was new to this game after all. shortly after this, we hired
           2 additional junior robotics engineers to assist with the development of the hardware and software

           <slide>
           I mean, hey the vendor had products which solved my problems right? And I could use them today? For Free?*
           We will get to that last part in a moment.

           It had some limitations. Lot's of limitations, but it worked for what we needed at the time.
           <slide>

           We managed to get Version 1 off the ground without too many late nights.
           However, we were also in the development phase of our system.
           Also known as the 'speggheti part'.
           <Show photo of first system's software>
           I also learned, that this phenomenon is not exclusive for software.
           <Show photo of first system>
           Now, in softare, we hide our shame with 14 layers of abstraction, and helper methods.
           In hardware, it's actually easier, you just lock the door.
           <show photo of closed box>
           We also had a lovely User Interface
           <Show V1 UI>
           Beauty really is in the eye of the beholder.

18:00 -    But it worked! We had our PoC. After 3 failed attempts
           <slide showing counter timers.>
           2 fires
           <slide showing hindenburg quickly.>
           and a lot of coffee.
           <slide showing coffee counter>
           We hit our goal of running the system for 24 hours without any deal-breaker issues. Success!

           In this process, we had started to get a hang of how our system worked. Both from a hardware and softare perspective.
           Ultimately version 1 was only about 1500 lines of code or so. We had not sunk too many resources into this just yet.

           Our UI was created by our vendor's free* UI Editor. It was impressive for a drag-and-drop editor. it also allowed
           us to get started with a GUI from the get-go. Minimal front-end development knowledge was needed, and our junoirs
           very quickly managed to hack something together that served what we needed it to do.

           Most importantly, we had delivered on a tight deadline. Not perfect, but enough to tick the box.

           We had built trust with management. And were shifting our focus on improving our hardware.
           Something which has a significanly longer development cadence than software.

           I knew if we were going to get some structure in our code. It was now or never.

           So naturally, I turned to the wonderful world of Reddit for advice on what libraries to use for development
           What the testing standards were, how they handled version control... The usual. SOme of oyu might even be a bit surprised
           why i mentioned version control in there.. We will get there, but
           <let me tell you something about reddit and advice..>
           I was promptly informed, in german no less,
           <slide>
           We don't do that here.
           <slide>
           Ok, why? But I kind knew why already.

           You see,
           The vendor we were using never charged us for some of their tools.
           This drag and drop UI editor is impressive for a no-code solutioin.
           Until the day we wanted to use the GUI to be avilable for more than a few days.
           One of juniors had experience with a different vendors GUI tools, and spoke wonders of
           our current vendors tool.
           Suddenly, we're hit with a popup:
           <slide>
           <slide>
           When we ran our Version 1, we were just under the 'free' allowance.
           Because free, did not mean free as in beer, it meant free as in "you can download and freely play around with
           this stuff where you will, inevendently, make something, and then we would have sucked you in, and now you will give us money because you've
           already invested significant effort and it's a pain to move" beer.

           Annoying, but fine, how much is this license?, 1000?
           <pause>
           ok, that's our coffee costs for i don't know. a day>
           <slide>
           dollars

            <pause>
            Clippy has betrayed me again.
           This is a bit rediculous.
           Oh, and for this 1000USD payment, you will get the privliedge of having a single-active-user. If you want to view the UI on mutliple screens
           on the same host, let alone across a network. That would be another USD200 per user.
           This is very rediculous.

           Suddenly this walled garden is showing some major cracks.
           But hey, it was a really nice drag and drop editor.
           And the vendor must have spent considerable effort builiding this product.
           Maybe 1000USD is just the cost of doing business. Again, I am a toursist in this industrial automation world.

           But a locally accessible UI was not the only requirement. I also needed to be able to interact
           with the device in an IoT context via AWS.
           I needed to store performance metrics, manage user credentials, automaticallt start this machine from anywhere in the world.
           In traditional programming, I would simply poll a server for a start command.

           And this, dear audiance, is where the 75 USD TCP request comes in.
           Our vendor might have spent considerable time on their drag-and-drop UI toy, but
           TCP is free. I can't, in good concious, pay for that.


           In truth, that was just the tipping point.
           Our hardware and software bills are coming to around 15000 USD. And this was still the PoC. There was no way
           that this 15000USD investment would ever see the commerical market. The PLC device our control code was running on cost 1000USD on it's own,
           and that's a lot of money to pay for a computer with same processing power as an intel celeron from 2010.

           At this point, if we proceeded with the traditoinal way of PLC development, we would be tying ourselves to this vendor indefintely

22:00 -    How we worked around these limitations, and what it means for us.
           We have already spent a lot of effort builing up the core control of our system. There was no way we could justify a rewrite of this, let alone to
           create an in-house runtime. We simply did not have the resources to do so. both financially and technically.

           Our experimental unit needed the safety aspects of the PLC.A lot of this requiers real-time performance.
           But not everything did. In fact, a lot of the overarching user-initiated logic could be offloaded to a general purpose computer.
           We used a NUC. Our specific trim of NUC was a order of magnitude more powerful, at half the price.

           Not only did we not need to do that part of the projet on the PLC, but we could also do that job far better in a language like python or
           go and make use of the entire library of code available, we still had reddit, but we also had 1000 other online communities to get shouted at from.

           If we had decided to implement this on the PLC. It would ahve taken us weeks to reimplement
           that 'one library in python' that solved this problem... a decade ago. We would also have to maintain whatever monstrosity we created.

           And why? Up to this point we've been foced to develop our system on windows. The vendor-provided editor is far from perfect. Basic tools like project-wide
           refactoring are still buggy and unusable. The editor crashes with 'error: error' constantly. If you try and debug the system too quickly after starting it. It permanently bricks your network connection, and only a hard reset seemed to solve that problem. And i'm being told 'this is just the way we do thing around here, kid'

           Looking beyond the short-term. The cost per unit of just the hardware would have been prohibitively expensive, and we could not easiily rewrite the sytem on
           a cheaper vendor due to our dependence on vendor-provided (and paid for) libraries, We would simply be swapping one devil for another.

           Your very expensive tool kit is not providing a satisfying user experience.
           Arguments I've heard as to why this cost (to my mental health,and wallet) are worth it
           range from 'this cost is pennies in the long run', Which would only start to be true, if you got
           to the long run.
           And ofcourse: Security Issues. These big companies surely have to be secure. For that peice.

           US Energy Grid hacks. These systems are no-more secure than any other. The closed source nature is a form of
           security via obsecurity, and any professional in the cyber-security field will scream their lungs out
           if you proposed that.


          How did we get here?

           All of this made sense in the 1980s when general purpose hardware and software really was not reliale. But this
           problem has been largely solved since then(Windows Aside), but this industry has not kept up. And this is going
           to cost them dearly.

           New entrants into the field are being crushed by a community that is exceptionally defensive of the way things
           have been done since the 80s. And maybe that's ok if you're using these PLC systems to control a dam, or your windfarms, but
           we've already seen it's not doing so well with the US electrical grid, and this is only going to get worse.

           This is creating a huge split in a community which is already fractured into smaller vendor-specific sub communities.

27:00 -    Why this behaviour in the industry will ultimately lead to stagnation.

           We have bunch of developers here. Who here knows what IEC-5002-I is? I thuoght so. Many of us
           are part of the current, previous,or next generation of engineers.

           The average age of Engineers proficient in this field is quickly approaching the sunset years. Fresh graduates are entering
           the Industral Automation Industry, and quickly realise that this skill set will pigeonhole there tehnical development.
           Younger engineers are expecting the same quality of life they had with traditional languages, as they should. Vendors
           are exceptionally slow, or even willingly neglegent, to implement these contemporary expectations.

           Single language solutions now dominate our web software industry. All sorts of libraries exist.

           'pip install httpx' does not come with a 75 USD price tag, and does a lot more than just TCP.

           None of this has happened in the Industrial Automation world. This is starting to smell awfully similra
           to the current traditional banking sector, and it's dependence on COBOL programmers. That industry has been stuck for years,
           and new companies with modern stacks, and attitudes are now serious competition.

           Machine demands are getting more and more intense. IoT, large data, AI Integrations, real-time observation.
           Engineering teams around the world are all making their own in-house versions for their specific vendors. Companies
           that create these tools view them as a market edge, and do not release them. These watered-down versions are sub-par,
           potentially leaking with security vulnerabilities,and just reinforcng the engineers dependance on the vendor.


29:00 -    Small Teams
           If someone more expereined, and maybe more sane was working with me at HYENA at the time.I don't tihnk
           we would have done waht we did. We faced a hostile and split community, almost zero vendor support, and honestly
           not enough experience to know what we were getting ourselves into.
           This could have ended up in ruin. I would be out of a job, and our dream of making Fuel Cells viable snuffed out before it even
           started.

           Small teams are either brazen, ignorent, or stupid enough to go against the grain. I am exceptionalyl greatful and impresesd
           by the team that assisted me in this project. Although, credit where credit is due.I feel like I was assiting them in the end.
           These are my collegues: Richard and Francesco. Combined, these fine genetlement had about 9 months of Industrial Automaion Expereicne when we started
           this project. If we include myself, we have just over a year.


32:00 -    In the course of a year, we managed to move all of our non-critical code to a locally networked device.
           We kept all the critical code on the PLC. we did end up paying our vendor for some licenses, but this bill came to about 100 USD.
           We also are able to keep 90% of code when we inevidently migrate to cheaper, embedded solution.
           At the same time we built and tested our first engineering units of our PowerPod.

           What started as Version 1<slide>

           became This;

           <slide>
           We still use what PLCs are good for. But we don't use them for everything. We broke free.

30:00 -    What happens next?
           We still are dependent on our vendor for the PLC system. The runtime environment they provide is still
           a major bottleneck. However, gone are the days where specific hardware is required to do this line of work. You don't need a specific PLC to do this work.
           It's high time that a hardware agnostic, open-source and modern competitor enters the arena. This world is chaanging. Finally, some PLC-like systems are supporting Linux.

           And while I will say, something of that nature is in them oven at HYENA, that talk will have to wait for another time.

33:00 -    In closing, I encourage all developers and engineers to seriously take a look at the tools and systems we use on a day to day basis
           and ask yourself just who is really in control of it's development, and future. Lastly, a huge thank you to my employer HYENA, for taking a risk on
           me and this project.

           Time will tell if three South Affrican Engineers were brazen, ignorent or stupid to take on 40 years of established industry norms.
           If anyone wants to conenct afterwards. Please come say hi. We are also hiring if this journey sounds exciting to you.
           <slide>

           These slides, as well as sources can be found on my github @wfletch or my personnelt website wfletch.com
40:00 -    End Of Talk

Mention explosiions and how we can't just seperate ouselves completely.
Use the hardware for it needs to do and no more.
Python gave us access to testing, linter tools that worked. IDE of choice.
And still no javascript <3 HTMX
Dare I say it. Customizable hotkeys.

