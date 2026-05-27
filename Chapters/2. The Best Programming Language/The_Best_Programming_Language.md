## The Best Programming Language for the AI era

Register A, load. Register B, shift. Compare. Branch if zero. That was the craft. That was the power. And then one morning, it simply wasn't needed anymore.

Back in the late 50s, programming meant speaking directly to the machine. Assembly programmers specified exact memory addresses, calculated every offset, managed every register by hand. One misplaced instruction and the entire system broke. Debugging meant staring at hexadecimal dumps on printed paper. These were highly skilled engineers — and they knew it.

Then COBOL arrived in the 60s, and shook the programming world like an earthquake. Suddenly the code had human-friendly words — business words that analysts could read, even if they couldn't write them. A new role was born: the analyst. And the Assembly programmers? They didn't vanish in a blink like the dinosaurs, it actually took a couple of decades, but there was no turning back. Over time, much of their work became unnecessary. You no longer needed to manage registers and memory addresses to process a payroll. COBOL handled that. The deep, hard-won mastery of talking directly to the machine — the very thing that defined these engineers — was being abstracted away.

**The appearance of COBOL wiped out some jobs, but it also created new ones.**

Some Assembly programmers adapted. They moved into systems programming, compilers, operating systems — areas where low-level control still mattered. Others became COBOL developers, trading their register-level mastery for a broader role in the business applications that were exploding in demand. 

Assembly programmers still exist today — not calculating bank transactions, but living deep inside compilers and embedded systems. It's estimated 70% of *financial* transactions still run in COBOL. And yet COBOL programmers are becoming impossible to find. Universities dropped it from their curricula. Senior programmers grow older with fewer replacements. 

**Change is like radiation, you don't feel it but it is all around you. And if you don't move quickly it'll kill you.**

Before I go there — let me be clear. If you have years behind you, real systems built, real failures learned from, the kind of calls that only experience teaches you to make — that matters. That does not go away. I am not about to tell you otherwise.

Now stop for a moment. Because right now, **you are the Assembly programmer of today**.

You are skilled. You interpret user stories, you make architectural decisions, you choose design patterns, you debug at 2am with nothing but a stack trace and intuition. Years of accumulated experience, perhaps a certification or two, or even more, the intuition that separates a good engineer from a great one. That is the craft. That is the identity.

And the ground has shifted. Not gradually — overnight. A new layer of abstraction has appeared above everything you spent years mastering.

With the arrival of Gen AI, the paradigm inverted:

**It's not us writing into an intermediate language, something in between human and machine language. The machine understands human language now.**

Just as COBOL abstracted away the Assembly programmer's register-level mastery, Gen AI is abstracting away the modern developer's syntax-level mastery. The deep, hard-won skill of writing code — the very thing that defines us — is being absorbed into a higher layer. Not eliminated. *Abstracted*. The difference matters, but the disruption is the same.

We've all heard about the layoffs. Some are real. Some are an excuse — AI as a flag to wave at investors, a narrative that justifies restructuring decisions that would have happened anyway. But beneath the noise, something true is happening: AI makes coding faster, and faster coding means smaller teams. Smaller teams mean fewer seats. Fewer seats mean the developer who would have been the sixth hire on a growing team is now never needed at all.

And for juniors — fresh out of university with four years of Java syntax in their heads — the situation is harder still. The entry-level coding work that used to be their training ground, their first rung on the ladder? AI has devoured it. You cannot become T-shaped the day you graduate. That takes time, exposure, mistakes, conversations with product owners at 9am on a Monday. That path is narrowing.

I won't pretend otherwise. The fear is real.

But here is what the Assembly programmers who survived understood, even without the words for it:

**You don't fight a river current. And you can't drop an anchor and expect the world to wait. You learn to read it — and it takes you places the swimmer struggling against it will never reach.**

---

The abstraction layers have been building for decades. Take, for instance, the Java chain: we write code in Java, then the compiler (written in Java) takes the `.java` files and generates `.class` files. The JVM (written in C++, with some C and assembly) takes those `.class` files and generates Assembly code in real time. If a new microprocessor arrives, the Assembly specialists create new intrinsic routines for the JVM — but new Java versions only require new C++ modules. We don't deal with the compiler anymore, just as we won't deal with the programming language syntax. Every generation of abstraction freed us to think at a higher level:

**Specs in human natural language are the new level of abstraction: Spec → Java → C++ → Assembly**

Imagine you are describing a feature to a colleague over coffee. No syntax. No brackets. Just clear thinking in plain sentences. Now imagine the machine was listening — and built it while you talked.

And here is where Spec-Driven Development enters the picture: fully human language instructions, no semicolons, no brackets, no operators, no strange character combinations — just plain human language. Like this book. I'm focusing in SDD and not in Vibe Coding because the later is not an structured SDLC practice.

It means that the English language — or whatever your human language is — will matter more than any programming language. Good grammar and clear thinking will carry the same weight as good syntax. High-level concepts will take more relevance than low-level ones. Design patterns, sometimes overlooked by developers who prefer to jump straight to the keyboard, will be more critical than naming conventions. Because you are not coding anymore. You tell the AI assistant how you like it — and let it do its thing. You focus on the *what*, not the *how*. I know the reality requires a extensive refining, back-and-forth discussions, Q&A with the AI, but every hour spent in clarifying definitions, establishing security and coding standards is worthwhile.

Today's Java code still looks like Klingon to business people:

int a = 2;
int b = 3;
int x = a << b + 1;

But with Spec-Driven Development, human language *is* the instruction — and the AI generates the code from it. You don't write the syntax. You describe what you need, clearly and precisely, and the machine does the rest.

In plain human language, that same operation reads:

"Calculate the value of `a` shifted left by `b` plus one, then store the result in `x`."


**Good grammar and spelling will matter the same as good programming language syntax.**

The Coding Guru used to be the person with the most tricks under their sleeve — all that accumulated experience, those edge cases memorized, those obscure methods known by heart. But all of that knowledge is now in the LLM's training data. The expertise has been democratized. The judgment has not.

**A good teacher once told me: you don't need to know all the answers, what you need is to know how to ask the right questions.**

To understand why, it helps to look at the shapes of developers.

The **I-shaped developer** is the deep specialist. Extraordinary expertise in one specific area — a rare programming language, a highly specialized backend domain, a SaaS platform few others know. When a long-running SQL stored procedure is grinding the system to a halt and nobody can figure out why, you call the I-shaped developer, your last line of defence as my first boss used to call me. But put them in a multi-disciplinary team meeting and they speak only their technical language — they struggle to translate their knowledge across domains or adapt when the problem shifts outside their vertical.

I know this from the inside. When I was a highly specialised Java engineer — one certification, the best problem-solver in the room — I could debug anything. But sitting across from a business user who wanted to change something I had spent weeks building? I struggled. I spoke Java. They spoke business. We were in the same meeting and somehow not in the same conversation.

**The developer who spends the next five years perfecting their syntax mastery in the AI era is making the same bet the Assembly programmer made in 1975 — and we know how that story ended.**

The **T-shaped developer** is different. They carry genuine expertise — say, Python or backend architecture — but also know enough about frontend, databases, cloud providers, and adjacent disciplines to wear multiple hats depending on the situation. They bridge. They translate. They can sit in a product meeting and then go implement.

The **π-shaped developer** is an evolution of one of those horizontal skills that grow to the point to become a mastery.

When I got my Java Web Component certification, without planning it, I became Pi-shaped. I could finally hear what the frontend team needed and translate it against the backend constraints. I became a bridge.

The **M-shaped developer**. Multiple peaks of expertise. Fluency across several disciplines, not just one. 

My Java Enterprise Architecture certification did the rest. Suddenly I had the full picture — not just the code, not just the flow, but also the infrastructure that moved the wheels, I fully understood the *why* behind the system. 

```
╔═══════════════════════╗   ╔═══════════════════════╗   ╔═══════════════════════╗   ╔═══════════════════════╗
║    I - S H A P E D    ║   ║    T - S H A P E D    ║   ║    Π - S H A P E D    ║   ║ C O M B - S H A P E D ║
║    E N G I N E E R    ║   ║    E N G I N E E R    ║   ║    E N G I N E E R    ║   ║    E N G I N E E R    ║
╚═══════════════════════╝   ╚═══════════════════════╝   ╚═══════════════════════╝   ╚═══════════════════════╝
░░░░░░░░░░█████░░░░░░░░░░   █████████████████████████   █████████████████████████   █████████████████████████
░░░░░░░░░░█████░░░░░░░░░░   █████████████████████████   █████████████████████████   █████████████████████████
░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░█████░░░░░░░░░░   █████░░░░░░░░░░░░░░░█████   █████░░░░░█████░░░░░█████
░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░█████░░░░░░░░░░   █████░░░░░░░░░░░░░░░█████   █████░░░░░█████░░░░░█████
░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░█████░░░░░░░░░░   █████░░░░░░░░░░░░░░░█████   █████░░░░░█████░░░░░█████
░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░█████░░░░░░░░░░   █████░░░░░░░░░░░░░░░█████   █████░░░░░█████░░░░░█████
░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░█████░░░░░░░░░░   █████░░░░░░░░░░░░░░░█████   █████░░░░░█████░░░░░█████
░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░█████░░░░░░░░░░   █████░░░░░░░░░░░░░░░█████   █████░░░░░█████░░░░░█████
░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░█████░░░░░░░░░░   █████░░░░░░░░░░░░░░░█████   █████░░░░░█████░░░░░█████
░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░█████░░░░░░░░░░   █████░░░░░░░░░░░░░░░█████   █████░░░░░░░░░░░░░░░█████
░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░░░░░░░░░░░█████   █████░░░░░░░░░░░░░░░█████
░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░░░░░░░░░░░█████   █████░░░░░░░░░░░░░░░░░░░░
```

`I made the verticals uneven on purpose because you cannot be a full-time expert in multiple areas unless you excercise them all on daily basis... which is the most common case.`

And AI multiplies what exists. It does not create what is missing, it won't make a vertical to grow out of nothing. The valleys stay valleys — and in an AI world, a valley becomes more dangerous, not less: the AI will generate plausible-looking work in your gap domain, and without the knowledge to evaluate it, you will not know it is wrong until production tells you. 

**Zero multiplied by AI still zero**

And AI fills the gaps on each area of expertise. So, if you're a π-shaped developer with good Java and decent React, you could potentialize the weak area (React in this case) with the help of AI. You can still judge the AI outputs because you have enough knowledge to see if they match your expectations. AI democratized the expertise but you still have to judge it.

```
╔═══════════════════════╗   ╔═══════════════════════╗   ╔═══════════════════════╗   ╔═══════════════════════╗
║    I - S H A P E D    ║   ║    T - S H A P E D    ║   ║    Π - S H A P E D    ║   ║ C O M B - S H A P E D ║
║    E N G I N E E R    ║   ║    E N G I N E E R    ║   ║    E N G I N E E R    ║   ║    E N G I N E E R    ║
╚═══════════════════════╝   ╚═══════════════════════╝   ╚═══════════════════════╝   ╚═══════════════════════╝
░░░░░░░░░░█████░░░░░░░░░░   █████████████████████████   █████████████████████████   █████████████████████████
░░░░░░░░░░█████░░░░░░░░░░   █████████████████████████   █████████████████████████   █████████████████████████
░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░█████░░░░░░░░░░   █████░░░░░░░░░░░░░░░█████   █████░░░░░█████░░░░░█████
░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░█████░░░░░░░░░░   █████░░░░░░░░░░░░░░░█████   █████░░░░░█████░░░░░█████
░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░█████░░░░░░░░░░   █████░░░░░░░░░░░░░░░█████   █████░░░░░█████░░░░░█████
░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░█████░░░░░░░░░░   █████░░░░░░░░░░░░░░░█████   █████░░░░░█████░░░░░█████
░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░█████░░░░░░░░░░   █████░░░░░░░░░░░░░░░█████   █████░░░░░█████░░░░░█████
░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░█████░░░░░░░░░░   █████░░░░░░░░░░░░░░░█████   █████░░░░░█████░░░░░█████
░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░█████░░░░░░░░░░   █████░░░░░░░░░░░░░░░█████   █████░░░░░█████░░░░░█████
░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░█████░░░░░░░░░░   █████░░░░░░░░░░░░░░░█████   █████░░░░░║   ║░░░░░█████
░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░█████░░░░░░░░░░   ║ AI║░░░░░░░░░░░░░░░█████   █████░░░░░║ AI║░░░░░█████
░░░░░░░░░░█████░░░░░░░░░░   ░░░░░░░░░░█████░░░░░░░░░░   ╚═══╝░░░░░░░░░░░░░░░█████   █████░░░░░╚═══╝░░░░░║ AI║
```

This brings an interesting question: Is coding still valuable?

Yes. But the honest answer is: less and less, and in different ways.

Large companies still need time to establish their AI standards, governance frameworks, and policies — and that takes years. There are millions of developers and not everyone will leap at once. Smaller companies will try to build their own software via Vibe Coding and come to us when their little Frankensteins need caging. Creating specs for large legacy systems will take years; in many cases it won't be worth the full effort, only for new features built on top.

**The lack of specs will become the technical debt of the future, the same way that the lack of unit tests haunts legacy applications today.**

Here is what that looks like in practice today. Take for instance a position we have open for several months: a high specialized and experienced C++ high-end engineer. We started looking in Europe... no results, then Latam... no results, then India... no results. After 6 months of searching it was clear that finding this person was the typical needle in a haystack. But what if we add a SDD specialist who can build the specs and let the Gen AI create highly specialized C++ code? The project would be saving months of searching and producing outcomes early in the schedule. And that differentiates a fast-paced company from slow-paced ones.

For people experienced in coding, this is a blow to their egos because that's what separates them from average developers. 

**But an *Augmented* average developer with AI mastery could match the experienced in the *coding field*.**

Now, these hyper-specialized roles normally are backed up by programming language certifications, they are expensive, take months to be ready and they elevate your status in LinkedIn. Actually, I remember when I coded heavily in T-SQL and thought a SQL programming certification might be worth pursuing. Then I changed companies, the landscape had moved, and T-SQL was a legacy tool. That certification would not have made me a better architect — it would have kept me in a golden jail, because people rarely abandon the things they suffered to earn. That's the Sunk Cost Fallacy — we defend what's ours, especially when it came at a high cost, even after the market has moved on.

Some other certifications I have — like TOGAF and Java Enterprise Architect — are different. Those are not language-fixed but architectural, conceptual, focused on building blocks. Those still matter.

So in my humble opinion — and it genuinely hurts me to say it, because I am a Java Certified Programmer — 

**Getting a language program certification today is not worth it**

That certification opened doors for me and I am grateful, and I'm not going to delete it from my resume and you shouldn't either. But I switched to .Net and that opened other doors. And as I progressed, I realized I had become language agnostic, almost without noticing.

The question stopped being *which language should I master* and became something entirely different:

**Why hyper-specialize in one language when you can speak them all?**

Recently I proved this to myself in a way I couldn't have imagined a few years ago. And it only worked because of something I had built over years before that project ever existed: I was already M-shaped.

A customer needed Python for a file migration project — several terabytes. I am not a Python developer. But I volunteered anyway, and because I had the breadth to step into every role — architect, PM, developer, reviewer — I ran the entire project end-to-end alone. The M-shaped profile was not the outcome. It was the prerequisite.

I started with a brainstorming session with AI agents. What surprised me was that the agents didn't just answer — they challenged me back. They asked questions I had overlooked. They raised what-if scenarios that genuinely enriched the discovery process. I came out of that session more confident and better prepared than I expected.

From there, I asked the PM Agent to build a comparison of different solution alternatives. The level of detail was remarkable — pages of structured pros and cons. I ran it multiple times as the project evolved, loading meeting transcriptions, vendor questionnaires, and requirements as they emerged. Everything accumulated into documentation that would have taken days of constant writing if done manually.

Then came the architecture. I worked with the Architect Agent to produce a Solution Architecture Document — customized with our company's SAD template, built around our standards. An SAD normally takes me one to two weeks. I had a solid initial version by lunchtime. After several rounds of revision, the epics and stories that followed were clean and sound.

Finally, I asked the Developer Agent to generate the code. It started with TDD — test-driven development — and produced working code in under an hour. An Adversary Agent reviewed it for code quality, which gave me confidence I wouldn't have had reviewing it alone.

Two tools built. One day. Python — a language I would never have chosen for myself. It was a simple, well-defined feature, guided by an expert, supported by thorough testing and feedback cycles. This isn’t magic, and I’m not here to sell smoke and mirrors. However, at the end of the day, every system is built from countless small user stories just like this one. 

We had estimated a Python developer in the Statement of Work for two weeks. They weren't needed at all.

I sat back at the end of that day with something I can only describe as bitter-sweet. The accuracy had surprised me — not perfect, I had to prompt corrections along the way, but the sheer volume of work compressed into a single day made those iterations feel trivial. We saved the customer money. We saved weeks of calendar. And yet — we could have hired someone. A person. That person was simply never called. The company also gave up some revenue. Whether that trade leads to more productivity and more projects, or to fewer jobs and leaner teams, I genuinely did not know. I still don't. What I knew, walking away from that day, was that I was an engineer holding a tool I hadn't yet fully learned to use — and that learning it was no longer optional.

What mattered was the architecture, the spec, the clarity of the *what*. The *how* took care of itself. It takes a lot of reading and iteration — building trust with the tool is a process, not a switch — but the results are worth it.

**And this is the real revolution. Java, Python and others will become the COBOL of the future.**

The current is moving. You cannot hold it still and you cannot outswim it. But you can learn to read it — to understand where it is going, to use it rather than fight it — and it will take you to places the swimmer exhausting themselves against it will never see.

The tools are already in your hands. The design patterns you know. The ability to sit with a product owner and turn a conversation into clarity. The instinct to structure a complex idea in plain language. These are not lesser skills in the AI era.

They are *the* skills.

**The best programming language for AI is English!**

And here is where it gets interesting. If English is now the programming language, then both the junior fresh out of university and the senior with twenty years of Java speak it fluently. For the first time, they are holding the same tool. So who wields it better — and who falls first?

*The answer might surprise you.*

