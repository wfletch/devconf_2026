00:00 -    Good Morning Devconf! I'm exceptionally excited to be here. This is actually my first presentation
           On Home Soil!

00:00 -    I'm here to talk to you today about this rather strange situation. How on earth did we find ourselves
           In the rather procerious situation of having to pay $75 for the privliedge to make a TCP request.
           in todays world... what possible situation could this even be?

00:00 -    So, without further pandering, let me tell you a story! But First. Who am i?
           My name is Warren Fletcher. I'm an electrical engineer who has spent far
           too much in the webscale world. In the past I've worked at Amazon, Oracle, and
           Booking.com. I've been privledged enough to work in multiple domains from performance optimzation
           to directly engaging with the customer.

00:00 -    In 2023, I returned from a stint in the Netherlands. While it was a life changing couple of years.
           I, quite frankly, missed the sun of South Africa. I also wanted to get my hands a bit dirtier when
           it came to my career and had an itch to get back into the wonderful world of hardware and electronics

02:00 -    Fortuantely, that itch was soon scratched when I joined HYENA as a Staff Engineer. A startup on the
           sunny, albeith windy, beaches of Muzimberg in Cape Town. Originally a spin out form UCT.
           HYENA aims to make the science fiction world of Fuel Cells a reality.
           And we are doing jus that, and specifically with a focus on the African market and
           our rather unique electrical grid and user needs.

03:00 -    Now, before we dive into the software. We should first discuss what a fuel cell is. and how we go around
           even using one. A Fuel cell, at it's core is simply a device which converts the chemical energy in
           in hydrogen to electrical energy. We can then use this electrical energy for all sorts of wonderful things.

05:00 -    Fuel Cell technology has been around for some time. Originally invented in 1839 by Sir william Christian Grove.
           The use of fuel cells was highly publicized in the 1960s when they were used on the Gemeini and Apollo space programs,
           and more recently, have been demonstrated to be usable in the transport and stationary power industries.
           Fuel cells, by their nature, require hydrogen. Hydrogen is not so easy to come by, and due to it's size requires
           some exceptioanlly strict storage and transportation requirements.

           This lack of avaiability, and getting the hydrogen to where it can be used has led us, as a socity, to remain addicted
           to hydro-carbon based fuel sources. So called Fossil Fuels. And while we generalyl focus on the carbon part. we neglect
           the hydro part, which as many of oyu have gathered, hydrogen. All hydro carbons (Natural Gas, LPG, Crude Oil) are hydrogen carriers

           Of all the hydrocarbons available. We specifically are interested in LPG and it's ubiquity to be found all over africa. Many of
           you have seen, or presently have LPG tanks for either heating or cooking. And while we are presently able to utalize the energy of
           LPG in the form of thermal energy by burning it. We would need a fuelcell to be able to use this same energy in its electrical form.

06:00 -    Our main product, the PowerPod takes this LPG from common LPG cylinders. Extracts the hydrogen from this fuel by a process known as reforming.
           I will spare everyone the details of this process, but it is important to know that is requires a very high temperature flame
           About 800 - 1000 Degress Celsius. REforming requires a lot of thermal energy, and this temperature needs to be maintained precisely to ensure we get optimal hydrogen
           Too much heat and the catalyst will decompose, too little and we won't produce enough Hydrogen. Thankfully, an entire industry exists
           to help us with just this task.


08:00 -    Industrial Automation.
           Industrial Automation is the intersection of hardware and software in a safety-critical environment with as little human involvement as possible.
           These projects very in size and complexity. But they are, above all, concerned with safety. And has been around for some time. Projets ranging from
           <Big project> to <small project> function because of the reliability and stability of Industrial Automation Systems.

09:00 -    And this industry has been around for some time. Originally it started in the 1980s, and has only been growing since.
           Specilized computing units known as a Programmable Logic Controllers were developed to handle these systems.

           The world, back then, was also a much simpler time. These devices pretty much just needed to read a sensor value, do some processing, and maybe make some sort
           of change via the adjustment of a valve or other actuator. This cyclic nature would continue indefintely

           This cycle or sampling some inputs, evaluating those inputs and then producing a output to be written to hardware is repeated 100s or even 100s of times a second.
           Timing is critical, and any jitter in the start of these cycles can lead to system instability. This jitter can be unafordable for sophisiticated motor control, let
           alone a critical infrastrucutre project with a price tag in the millions, or billions or dollars.

           And PLCs did one hell of a great job. This industry grew, and many hardware manufactuers saw the commerical opportunity of delivering and mainting these specialized hardware devices.

12:00 -    What does this mean in a modern context
           The problem with specilized hardware is that vendors need to make hardware, and this hardware needs to be controlled. This has led to a prolifiration of vendor-locked
           frameworks. While these systems may speak the same languages, they all use slightly different veriations that just so happen to be tailored to the specifics
           of the hardware that the company is trying to sell you, and are completely incompatible with competitors systems.
           Say what you will about oracle and their exorpatend prices for the Jave Enterprise JRE. At least they don't force to you use a specific processor.

           And while it may seem convenient that the software you use will run. It also leads to a companies engineering team being in some part limited
           by the whims on your chosen hardware partner.Eventually, over time, you end up with staff who only know a single vendors product. This limits both the
           indivdual engineer, as well as the companies abilities to grow.

           We actualyl have a term for such a sitation. It's called a walled garden, and they are very prevalent in
           todays society. Weather by choice or by chance. Most fameously, Apple.
           Yes. I use a lot of apple products. Hell, I would stop just sort of saying I like apple Products.
           Great for the company making the garden (Apple). Less great for the
           attendee of the garden.

15:00 -    So let's go back to a slightly younger version of myself. I need accuretly control a flame and a chemical reaction that produces hydrogen.
           I've got a PLC system from a vendor, and Ive just come out of a very different world. The stack at my disposal to implement these solutsions
           was completely defined by the vendor. But hey, the vendor had products which solved my solutions right?
           It had some limitations. Lot's of limitations, but it worked for the simple things. Until it didnt. Google results turned up nothing.
           We changed the language to german and we can't some obscure hits that helped. It was so difficult to find information on this topic,
           taht even chatGPT (in 2024) just said it didnt know.
           <We need to include information about the uncertainty of our system>
           <How we build a library to assist us in this chop and change of parts>
           <Significant research yielded a shocking amount of libraries. nothing Stable to be precise>
           <Mention how, from a product perspective, we always knew we would not be able to sell this product. Some AWS Reference on image sizes>

18:00 -    But we persevered, and managed to reach all our functional goals within our time budget.
           The vendor we were using never charged us for some of their tools.
           This drag and drop UI editor is impressive for a no-code solutioin.
           Until the day we wanted to use the UI in production. suddenly we're hit with a license requirement.
           Annoying, but fine, how much is this license? $1000.
            <pause>
           This is a bit rediculous.
           Oh, and for this 1000USD payment, you will get the privliedge of having a single-active-user. If you want to view the UI on mutliple screens
           on the same host, let alone across a network. That would be another USD200 per user.

           Suddenly this walled garden is showing some major cracks.
           But hey, it was a really nice drag and drop editor.
           And the vendor must have spent considerable effort builiding this product.
           Maybe 1000USD is just the cost of doing business.

           But a locally accessible UI was not the only requirement. I also needed to be able to interact
           with the device in an IoT context via AWS. I needed to store performance metrics, manage user credentials,
           ... < a third cost>
           Suddenly our hardware and software bills are coming to around 15000 USD. And this was still the PoC. There was no way
           that this 15000USD investment would ever see the commerical market.

           And this, dear audiance, is where the 75 USD TCP request comes in.
           Our vendor might have spent considerable time on their drag-and-drop toy, but
           TCP is free. I can't, in good concious, pay for that.


22:00 -    How we worked around these limitations, and what it means for us.
           We have already spent a lot of effort builing up the core control of our system. There was no way we could justify a rewrite of this, let alone to
           create an in-house runtime. We simply did not have the resources to do so.

           Our experimental unit needed the safety aspects of the PLC.A lot of this requiers real-time performance.
           But not everything did. In fact, a lot of the overarching user-initiated logic could be offloaded to a general purpose computer.
           We used a NUC. Our specific trim of NUC was a order of magnitude more powerful, at a quarter of the price.

           Not only did we not need to do that part of the projet on the PLC, but we could also do that job far better in a language like python or
           go and make use of the entire library of code available. If we had decided to implement this on the PLC. It would ahve taken us weeks to reimplement
           that 'one library in python' that solved this problem... a decade ago. We would also have to maintain whatever monstrosity we created.

           And why? Up to this point we've been foced to develop our system on windows. The vendor-provided editor is far from perfect. Basic tools like project-wide
           refactoring are still buggy and unusable. The editor crashes with 'error: error' constantly. If you try and debug the system too quickly after starting it. It permanently bricks your network connection, and only a hard reset seemed to solve that problem.

           Looking beyond the short-term. The cost per unit of just the hardware would have been prohibitively expensive, and we could not easiily rewrite the sytem on
           a cheaper vendor due to the slight oddities of our current one.

           Your very expensive tool kit is not providing a satisfying user experience.
           Arguments I've heard as to why this cost (to my mental health,and wallet) are worth it
           range from 'this cost is pennies in the long run', Which would only start to be true, if you got
           to the long run.
           And ofcourse: Security Issues. These big companies surely have to be secure. For taht pice.

           US Energy Grid hacks. These systems are no-more secure than any other. The closed source nature is a form of
           security via obsecurity, and any professional in the cyber-security field will scream their lungs out
           if you proposed that.

           Just use a different vendor? Everone in the industry. All these vendors are playing this walled garden game to some
           degree.

           This is what happens when their is no open-source or cheap alternative.

           All of this made sense in the 1980s when general purpose hardware and software really was nto reliale. But this
           problem has been largely solved (Windows Aside), but this industry has not kept up.

           New entrants into the field are being crushed by a community that is exceptionally defensive of the way things
           have been done. And maybe that's ok, but it won't be ok for ever. This is creating a huge split in a community
           which is already fractured into small sub-communities tied to the users choice of vendor.


27:00 -    Why this behaviour in the industry will ultimately lead to stagnation.

           We have bunch of developers here. Who here knows what IEC-5002-I is? I thuoght so. Many of us
           are part of the current, previous,or next generation of engineers.

           The average age of Engineers proficient in this field is quickly approaching the sunset years. Younger engieers are expecting
           the same quality of life they had with traditional languages.

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
           we would have done waht we did. We faced a hostile and split community, lmost zero vendor support, and honestly
           not enough experience to know what we were getting ourselves into.
           This could have ended up in ruin. I would be out of a job, and our dream of making Fuel Cells viable snuffed out.

           Small teams are either brazen, ignorent, or stupid enough to go against the grain. I am exceptionalyl greatful and impresesd
           by the team that assisted me in this project. Although, credit where credit is due.I feel like I was assiting them in the end.
           These are my collegues: Richard and Francesco. Combined, these fine genetlement had about 9 months of Industrial Automaion Expereicne when we started
           this project. If we include myself, we have just over a year of combined.


32:00 -    In the course of a year, we managed to move all of our non-critical code to a locally networked device.
           We kept all the critical code on the PLC. we did end up paying our vendor for some licenses, but this bill came to about 100 USD.
           At the same time we built and tested our first engineering units of our PowerPod. What started as This became This;

30:00 -    What happens next?
           We still are dependent on our vendor for the PLC system. The runtime environment they provide is still
           a major bottleneck. However, gone are the days where specific hardware is required to do this line of work.
           It's high time that a hardware agnostic, open-source and modern competitor enters the arena. And while I will say, something of that nature is in the
           oven at HYENA, that talk will have to wait for another time.

33:00 -    In closing, I encourage all developers and engineers to seriously take a look at the tools and systems we use on a day to day basis
           and ask yourself just who is really in control of it's development, and future. Lastly, a huge thank you to my employer HYENA, for taking a risk on
           me and this project.

           Time will tell if we we brazen, ignorent or stupid to do what we did. Thank you.
           If anyone wants to conenct afterwards. Please come say hi. We are also hiring if
           this journey sounds exciting to you.


40:00 -    End Of Talk

Mention explosiions and how we can't just seperate ouselves completely.
Use the hardware for it needs to do and no more.
Python gave us access to testing, linter tools that worked. IDE of choice.
Dare I say it. Customizable hotkeys.

