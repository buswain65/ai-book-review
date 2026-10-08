# Chapter 1: Hotfix

At 4:55 on a Thursday afternoon, Walter Dunleavy had his coat on, his laptop closed, and one arm already through the strap of his bag. It was a rare alignment of the planets, and he intended to make the most of it.

He had a plan. As plans went, it was modest. It involved going home, eating something that had not come out of the office vending machine, and lying on his couch in a state of total, uninterrupted not-working until he fell asleep. In Walter's experience, a plan like that had roughly the same odds as a lottery ticket, which was why he hadn't told anyone about it.

He made it four steps toward the elevator.

"Walt! Walter. Walt-man."

There were three people in the world who called him Walt-man. Two of them were his nephews, who were six. The third was Trent Vollmer, founder and CEO of SynergyStack, who was crossing the open-plan floor with his phone held aloft like the Olympic torch.

Trent wore a fleece vest over a button-down shirt, the official uniform of men who had raised a Series B. He had very white teeth and the boundless, frictionless energy of someone who had never personally had to do anything he'd promised.

"Great news," Trent said. "Just got off with the Hendricks people. Huge account. *Huge.* They're seeing a little thing in the export module. Tiny. Basically cosmetic. I told them we'd have a fix out by morning."

"By morning," Walter said.

"First thing. It's small. You'll knock it out in an hour."

Walter knew, the way other men know their own shoe size, that it was not an hour.

The export module was fourteen thousand lines of code written by four people, three of whom no longer worked at SynergyStack and one of whom was Trent. Nothing in the export module was tiny. Nothing in it was basically cosmetic. The fix, whatever it turned out to be, would take three days. Three days if nothing went wrong, and something always went wrong.

This was the one real talent Walter had. He could look at a piece of work and simply *know* how long it would take. Not guess. Know. He had been right about every project for nineteen years. In all that time, the talent had never once been useful, because nobody had ever wanted to hear the number.

He opened his mouth to say *That's three days, Trent.*

What came out was: "Sure. I'll take a look."

"That's my guy!" Trent clapped him on the shoulder and pointed at the wall behind Walter's desk, where the company values were painted in tall white letters. "Ownership! That's what it's all about."

Walter didn't need to turn around. He knew the wall by heart. **OWN IT.** **MOVE FAST.** **NO SURPRISES.** **WORK HARD, REST HARDER.** The last one had been added after an anonymous employee survey, and at the time Walter had thought it was the funniest thing he'd ever read.

"I'd stay and help," Trent said, already walking backward toward the elevator, "but I've got a thing." The thing, Walter would learn later from the company newsletter, was a podcast appearance on the subject of founder burnout.

The elevator doors closed on Trent's teeth.

Walter stood alone for a moment in the middle of the floor. Then he took off his coat and hung it on the back of his chair, where it would stay, as things turned out, for the rest of his life.

---

At 5:50, Josh appeared at the edge of Walter's desk. He had a backpack over one shoulder and a black apron folded under his arm.

Josh was twenty-four and in the third year of a six-month internship. He had the bright, unbreakable optimism of someone who had not yet been at SynergyStack long enough to stop having it. Walter had been watching for two and a half years, waiting for it to wear off. So far, it hadn't.

"You're still here," Josh said.

"Hendricks," said Walter.

"Oh no." Josh winced. "The export thing? I heard Trent on the phone. 'Basically cosmetic.'" He did a fairly good Trent: chin up, teeth out. "How long is it really?"

Walter looked at him. No one at SynergyStack had asked him that question in about four years. Trent never asked, because he already knew the answer he wanted. The managers never asked, because the answer would have to go in a status report. Josh asked because he wanted to know.

"Three days," Walter said. "If nothing goes wrong."

Josh nodded slowly, as though Walter had just told him the weather. "And something always goes wrong."

"Something always goes wrong."

"I could stay." Josh was already pulling out his phone. "I can call out of my shift. Marco won't care. Okay, Marco will care, but he'll get over it."

For a moment Walter was tempted. Then he thought about the apron, and the restaurant, and the fact that Josh's second job was the one that actually paid him.

"Go," Walter said. "Seriously. It's one fix. I've got it."

"You sure?"

"Sure."

Josh hesitated, then dug into his backpack and set a granola bar on the desk with great ceremony, like a knight leaving a sword at a shrine. It was the expensive kind, with chocolate in it.

"For emergencies," he said.

"Thanks, Josh."

"Hey, so, good news, by the way." Josh lowered his voice. "Craig said my full-time offer is basically done. They're just waiting on budget."

Craig had told Josh this in March. And last October. Walter had seen the budget spreadsheet once, by accident, and the intern-conversion line had a zero in it and a comment that said *revisit Q4*. It had said *revisit Q4* for three years.

"That's great," Walter said, and hated himself a little.

"Right?" Josh beamed. "Okay. Don't stay too late." He was halfway to the elevator when he turned around. "Oh! Did you know the 'G' in all those code comments is a guy named Gary? Dana told me before she left. He built the whole back end. Apparently he moved to Oregon to raise alpacas."

"I've heard," Walter said.

"Wild," said Josh happily. "Imagine just *leaving*." And the elevator doors closed on him, still smiling.

Walter put the granola bar in his top drawer, where it would turn out to be the last thing anyone ever gave him on Earth.

---

The export module, when Walter opened it, greeted him like an old enemy.

The first function was called `doExport`. It called a function named `doExport2`, which called `doExportNew`, which called `doExportNew_FINAL`, which called `doExport`. Walter had spent most of a week in 2023 trying to understand how this didn't simply run in a circle forever. He had eventually concluded that it did, and that something else, somewhere else, was quietly stopping it. He had never found out what. He had decided that he didn't want to know.

Above the worst of it sat a single comment, left by a previous engineer:

`// TODO: fix this properly. Don't ask. —G`

Walter did not ask. There was no one to ask. He cracked his knuckles and got to work.

At 6:40 p.m., his laptop made the soft, cheerful *bloop* of an incoming message on Ping, the company chat app. Walter had come to hate that sound with an intensity normally reserved for dentists.

It was Brynn Castellano, Senior Product Manager.

> **Brynn:** hey!! quick q :) while you're in there, can the export also include archived records? hendricks mentioned it. tiny thing

Walter looked at the message. In his head, quietly, the three days became five.

> **Walter:** That's not really part of the fix. Archived records are in a different database.
>
> **Brynn:** oh totally, no pressure!! just if it's easy

It was not easy. Brynn knew it was not easy, in the way that everyone at SynergyStack knew things were not easy and had collectively agreed to pretend otherwise. *No pressure* was what people at SynergyStack said instead of *this is now your problem.*

> **Walter:** Sure. I'll take a look.

At 8:15 p.m.: *bloop.*

> **Brynn:** ok so update!! hendricks wants the export as a PDF too. should be easy since it's the same data right?

Five days became eight.

At 8:52 p.m.: *bloop.*

> **Brynn:** \[attachment: export\_mockup\_v3.png\] **Brynn:** also, they asked if the export button could be purple? i said probably!! :)

Walter opened the mockup. It showed the export screen exactly as it already existed, except that the button was purple and there was a new checkbox labeled *Include Everything*. Nobody had ever defined what *Everything* was. Walter suspected that nobody ever would, and that he would be blamed for whatever it turned out not to include.

Eight days became eleven.

> **Brynn:** ok heading out!! you're a rockstar. this is gonna be SO good for the Q3 numbers

Her status light went gray. Walter sat back in his chair and looked at the ceiling tiles, which were the color of old oatmeal and had been there, according to office legend, since before the building had a name.

The fix was still due by morning. It was now, by Walter's private and perfectly accurate reckoning, eleven days of work.

He went to get a coffee.

---

By ten o'clock, the office had taken on the particular silence of a workplace after hours. It was a hum made of servers, ventilation, and the faint buzzing of one fluorescent tube that Facilities had been "looking into" since March.

The walk to the coffee machine took Walter past the engineering pod. There had once been nine engineers in it. There were now four, which Trent described in all-hands meetings as "running lean" and which the remaining four described, privately, in other terms.

The first empty desk belonged to Dana Okafor, who had been the company's only QA engineer until the spring "rightsizing." Her desk had never been cleared. Her stress ball, shaped like a bug, still sat beside her monitor, along with a little laminated sign that read: **IT IS NOT A FEATURE.** After she was let go, Trent had announced that SynergyStack was "embracing a culture where everyone owns quality." In practice, this meant that nobody tested anything. Bugs were now found by customers, which Trent called "real-world validation."

Walter missed Dana. She had broken everything he ever built, and she had always been right.

The next desk belonged to Josh. His chair was pushed in neatly, the way it always was, and a sticky note on his monitor read *ask Walter re: estimates??* At this moment, Walter supposed, he was carrying plates of linguine to people who tipped badly.

The coffee machine, a gleaming Italian model with more buttons than the export module had tests, produced something brown and furious. Walter carried it back to his desk.

At 10:31 p.m., an email arrived from the VP of Engineering. It had been sent to the entire Hendricks account team, which consisted of four engineers and seven managers:

> **Subject:** Hendricks fix — great work, team!
>
> Just want to recognize the incredible ownership on display tonight. This is what SynergyStack is all about. Let's bring it home!

Within ten minutes, the email had received five replies. They came from the Director of Engineering, the Engineering Manager, the Head of Delivery, Brynn, and someone named Craig whose job title was "Strategic Alignment" and whom Walter had never seen in person. All five said some version of *Great work, team!* Two of them included a GIF. None of them had been in the building since 5:30.

The seventh manager was Trent, who replied-all from the podcast studio with a single word: **"Legends."**

Walter did the math, as he always did. Seven managers. Four engineers. One of the four engineers — him — actually awake and working. That meant every hour Walter spent on the fix was supervised by seven people, all of whom were at home.

He looked around his desk and, in a rare moment of introspection brought on by caffeine and despair, took a kind of inventory of his life.

There was a succulent in a little ceramic pot. It had been a gift from his sister. Succulents are famously the hardest houseplant on Earth to kill. Walter's had been dead since February.

There was a gym membership card, used twice, both times in January.

There was a framed photo of his nephews at the beach, from a trip he hadn't gone on because of a release.

In his inbox, unread for three weeks, sat a message from Human Resources titled **Prioritize Your Wellness!** It contained a link to a meditation app and a reminder that the company's mandatory forty-five-minute Wellness Training was due by Friday.

And in the HR portal, which he opened only to confirm what he already knew, his unused vacation balance stood at **sixty-three days**. SynergyStack had an official use-it-or-lose-it vacation policy. It had never been enforced, because no one had ever used it.

His phone buzzed. A text from his sister, sent Tuesday, which he'd somehow never answered:

> **Megan:** dinner sunday? the boys want to show you their volcano

Walter looked at it for a long moment. Then he typed *Sure. Wouldn't miss it* and hit send, and believed it, the way he always did.

Then he turned back to the export module. It was 11:47 p.m., and the fix wasn't working, and he had a feeling — the old, certain, shoe-size feeling — that he knew exactly why.

---

He spent the next two hours trying to prove himself wrong.

Every engineer knows this technique. When you suspect the problem is something terrible, you first rule out everything that isn't terrible, in the hope that one of the harmless things turns out to be guilty. It almost never works. Engineers do it anyway, the way people check the same empty pocket three times for their keys.

He restarted the export service. Nothing.

He cleared the cache. Then the other cache, the one nobody remembered setting up. Then a third cache, hidden inside the second. For one terrible moment, every customer's name on the company dashboard read "undefined." He put the third cache back.

At 12:15, the motion-sensor lights decided the building was empty and switched off. Walter waved both arms over his head like a man flagging down a rescue helicopter. The lights came back on. He would do this four more times before the night was over.

He made the button purple. It took forty seconds, and it was the only thing all night that went according to plan. It was, he had to admit, a nice purple.

He tried the PDF. The PDF library needed version 4 of a tool called `datefmt`. The rest of the export needed version 2, and refused to start if version 4 was anywhere in the building. Walter spent half an hour trying to get them to share. It was like hosting Thanksgiving for divorced relatives. Finally he wrote *PDF — Monday* on a sticky note, knowing the note was a lie.

He searched online for the error message. One result: a forum post from 2011 by a user named `gary_builds_things`, describing Walter's problem in perfect detail. Under it sat a single reply from `gary_builds_things`, three days later:

> nvm fixed it

No explanation. No code. Just the permanent satisfaction of a man who had solved a problem and taken the answer with him to Oregon.

Walter stared at it for a long time.

Then, because there was nothing left to rule out, he opened the network logs.

At 1:52 a.m., the logs confirmed it.

Every time the export ran, it sent a request to a machine on the internal network called `floozie-01`. The request waited exactly thirty seconds. Then it gave up and failed. No one at SynergyStack had written the code that sent that request. No one at SynergyStack, as far as Walter knew, had ever agreed that the export should depend on `floozie-01`. But somewhere inside the endless loop of `doExport`, `doExport2`, `doExportNew` and `doExportNew_FINAL`, it did. It always had. Very possibly, it was the thing that stopped the loop.

Walter closed his eyes.

Everyone at SynergyStack knew about Old Floozie. Very few people had seen her. She lived in the server closet at the end of the hall, behind a door with a broken lock and a hand-lettered sign that read **AUTHORIZED PERSONNEL ONLY**. No one was authorized. No one had ever been authorized. The sign predated the company's current lease.

He went to look at her anyway.

Old Floozie was a server rack, six feet tall and the color of a nicotine stain. She dated, by Walter's best estimate, from around 2009, which in computer years made her roughly the age of the pyramids. Cables spilled out of her front in great tangled loops, red and blue and yellow and gray, some of them labeled, most of them not. Two of the labels said **DO NOT UNPLUG**. One said **UNPLUG IF HOT**. One said **???**. Her fans produced a low, wheezing whine, like an elderly relative who had opinions about your career.

Taped across her front, curled and yellow with age, was a single sticky note:

**DO NOT TOUCH — ask Gary**

Gary had left SynergyStack in 2014. According to office legend, he'd gone to raise alpacas in Oregon. Nobody had his phone number. The only documentation Gary had ever left behind was a text file on Floozie's main drive called `README_IMPORTANT.txt`. Walter had read it once, years ago, in a moment of hope. In full, it said:

`you know what to do`

No one knew what Old Floozie did. Everyone knew what happened when she stopped doing it. In 2019, a night cleaner had unplugged her to vacuum. In the twenty minutes before someone plugged her back in, payroll went down, the building's badge readers stopped working, the coffee machine began dispensing only hot water, and one of the elevators played "The Girl from Ipanema" on a loop for three days. Nobody ever found the connection. Nobody ever looked very hard.

Old Floozie had outlasted four CTOs, three office renovations, two "cloud migrations" and a company rebrand. Every engineer who had ever worked at SynergyStack had, at some point, logged into her late at night and changed something they shouldn't have, and then quietly never mentioned it again. That was what people meant when they said, with a certain tone, that Old Floozie had "been with every engineer in the building."

Walter crouched down with his phone's flashlight and followed the export's network path to the back of the rack.

There it was. Low down near the floor, behind her, in the narrow gap between Old Floozie and the wall: one network cable, half pulled out of its port. Just loose enough to time out. Just connected enough to look fine on every monitoring dashboard the company had ever paid for.

The fix was to push it back in. That was all. Ten seconds of work. Except that the cable was behind six feet of ancient, top-heavy server rack, wedged against a wall, in a closet nobody was allowed to enter, under a note that said not to touch anything.

Walter went back to his desk and did something he almost never did. He wrote down the truth.

> **Walter → Trent:** The fix isn't an hour. It's not a night either. The export depends on Old Floozie, nobody knows how, and doing this properly is about eleven days of work. I can patch it tonight, but it means touching Floozie. I don't think I should.

He read it over three times. It was accurate. It was reasonable. It was, he was quite sure, the most honest message anyone had sent on Ping in the history of the company.

He thought about the next morning. Trent's face. The words *culture of ownership*. The meeting about the message, and the meeting about that meeting. The five managers who would reply-all to ask whether "eleven days" was "really eleven days or more of a directional number."

He deleted it.

It was 2:58 a.m.

---

The closet floor was crowded with the archaeology of a startup. Walter had to move three boxes to get close. One was full of conference lanyards. One held unopened packs of business cards for a job title that no longer existed. The third was full of T-shirts from the 2017 company hackathon, printed with the slogan **SLEEP IS A BUG**.

He got down on his knees in front of Old Floozie. Up close, her fans sounded less like a whine and more like breathing.

"Hi," Walter said, because it was three in the morning and there was no one else to talk to. "I'm just going to fix one thing. Then I'm going to go home. Okay?"

Old Floozie wheezed.

He noticed, as he leaned in, that the rack wasn't standing level. One of her front feet rested on a thick, folded wad of paper that someone had jammed underneath to stop her rocking. He tilted his head to read the spine. It was the SynergyStack Employee Handbook, 2014 edition. In all his years at the company, it was the first time Walter had seen anyone use the handbook for anything.

He lay down on his side on the cold floor and stretched his arm into the gap behind her.

It was a long reach. He had to push his shoulder against the side of the rack to get there. His fingertips brushed cables — warm ones, cold ones, one that was alarmingly sticky — and then, at the very limit of his arm, he felt the loose plug.

And lying there in the dark, with his cheek on the floor tile, Walter had a very clear thought. It arrived the way his estimates always did: complete and certain, without being asked for.

*You've said "Sure, I'll take a look" about four thousand times.*

It wasn't a voice. It was just math. Nineteen years. Five workdays a week, give or take the weekends, which had stopped counting as weekends a long time ago. Every "sure" had felt like a small, harmless thing — an hour here, a night there. Nobody had ever told him what they added up to. He had never once sat down and done the math, which was strange, because math was the one thing he was good at.

He was going to do it differently, he decided. Starting Monday. He'd take some of the sixty-three days. He'd go to Megan's on Sunday and look at the volcano. He'd tell Trent the real number, the next time, and let the five managers reply-all about it.

He pushed the cable home.

It went in with a small, satisfying *click*. On his laptop, back on his desk down the hall, a progress bar began to move.

Walter pulled his arm back. As he did, his shoulder shoved the side of the rack, just a little — just enough to slide the 2014 Employee Handbook out from under Old Floozie's front foot.

There was a pause, of the kind that happens in cartoons. During it, Walter heard several things at once: the wheeze of her fans, the buzz of the broken fluorescent tube out in the hall, and a slow, deep creak, like a ship deciding something.

Then Old Floozie — six feet tall, three hundred and forty pounds, fifteen years of everyone's undocumented secrets — leaned gently forward and came to rest on top of him.

She did it, all things considered, with a kind of tenderness.

It did not hurt as much as Walter would have expected. Mostly he felt surprise, and then a sort of weary recognition, as if he had known this was coming for a very long time and simply hadn't put a date on it.

His last thought on Earth was not of his sister, or the nephews, or the volcano, or the sixty-three days. It was the thought of an engineer who has just figured out, too late, exactly what the problem was.

*I should've written that down.*

---

Down the hall, on Walter's desk, the deploy bar crawled to 99% and stopped.

In the closet, Old Floozie's fans whirred down to silence. Across the building, the badge readers went dark. The coffee machine began dispensing hot water. Somewhere far off, an elevator started, softly, to play "The Girl from Ipanema."

At 3:13 a.m., Walter's laptop went *bloop.*

> **Trent:** any update?

And somewhere much, much farther away, in a place with no clocks, a take-a-number machine whirred to life, and printed a ticket.
