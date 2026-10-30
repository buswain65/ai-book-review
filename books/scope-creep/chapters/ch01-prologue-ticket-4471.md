# Prologue: Ticket #4471

At 11:52 p.m. on a Tuesday, Mike Dobbins of Raleigh, North Carolina, was forty-four years old, eleven years into his job at Synergex Solutions, and wearing the same NC State Wolfpack hoodie he'd been wearing since Sunday.

His phone buzzed. Then it buzzed again. Then it started ringing, which at Synergex meant someone in a corner office had discovered the phone app.

"Mike, buddy." It was Chad Pemberton, CEO, calling from what sounded like a golf simulator bar. "Hartwell Logistics is down. Their guy called me personally. *Personally*, Mike."

"Hartwell is always down," Mike said. "Hartwell's guy calls you personally every Tuesday. Last week he called because his mouse was unplugged."

"This is different. He used capital letters."

Mike closed his eyes. Somewhere behind them, a vein he'd been meaning to have looked at since 2019 began to throb.

Hartwell was Synergex's biggest client, which meant Hartwell's head of operations, a man named Doug who typed exclusively in caps lock, had effectively been running the company's roadmap for six years. Every feature Doug wanted was urgent. Every bug Doug found was a crisis. Every midnight was, potentially, Doug's.

"What's actually broken?" Mike asked.

"The new routing thing. The thing Brittany sold them."

Ah. The thing Brittany sold them.

Three weeks ago, in a sales meeting Mike had not been invited to, Brittany from Enterprise Accounts had told Hartwell that Synergex's platform "already basically" supported real-time multi-depot route optimization. It did not. It did not basically do it, or approximately do it, or do it in the sense that a sketch of a car is basically a car. But Hartwell had signed a three-year renewal, Brittany had rung the little brass gong in the sales pit, and the next morning a ticket appeared in Mike's queue titled simply: **ROUTING (SOLD).**

Chad had asked him for an estimate. Mike had said, "I genuinely don't know. Maybe two weeks if nothing's weird. But something's always weird."

Chad had written *2 weeks* on a whiteboard, photographed it, and emailed the photo to Hartwell with the subject line **COMMITTED!**

When day fifteen arrived, Mike had been called into a meeting with HR about "accountability gaps."

The routing feature had shipped on day nineteen. No code review, because the other senior dev had been reassigned to an emergency "quick win" for Chad: moving the login button to the left side of the screen, which had somehow required rewriting the authentication system, which was why the login page now occasionally logged you in as a different person. And the requirements had changed four times during the build, most recently when Doug decided the routes should also "factor in weather, like vibes-wise."

And now it was down.

"I'll go in," Mike said.

"You're a rock star, buddy. I'll tell Doug you're on it. Oh, and Mike? When you get a sec, we should talk about why this keeps happening with your code."

---

The office was dark except for the server closet and the break room, which facilities had relocated over the weekend because Chad wanted the old break room for a "podcast studio." When the electrician had raised concerns about the wiring, he'd been told it was "just moving a coffee maker."

Mike found the bug at 2:10 a.m. It was a hardcoded assumption that no truck would ever visit more than one depot, made eighteen days earlier by a sleep-deprived man named Mike Dobbins under direct orders to "just get it working for the demo." He fixed it, tested it, couldn't get anyone to review it, deployed it anyway, and watched the error dashboard slowly turn from red to green.

At 3:47 a.m., the Hartwell system was back up. Mike leaned back in his chair and allowed himself one small, private feeling of triumph.

Then he went to make a victory coffee.

The coffee maker was in its new spot. Its new spot had a new outlet. The new outlet was, it would later be determined, wired to a circuit that also ran through the decorative fountain in the podcast studio.

Mike Dobbins pressed BREW.

His last conscious thought was not about his life, or his regrets, or the vein. It was: *Somebody is going to blame this on my code.*

They did. The incident report cited "an unstable deployment immediately preceding the event."

---

He woke up in a waiting room.

It had beige carpet and a take-a-number dispenser, and a sign reading **NOW SERVING: 88,412,907**. Mike looked at the paper slip in his hand. It said 88,413,544.

Four hours later, a harried woman with luminous wings, three pens stuck in her hair, and a lanyard reading **GODDESS OF TRANSITIONS — TIER 2 SUPPORT** finally called his number.

"Dobbins, Michael. Death by..." She squinted at a scroll. "Coffee maker. Huh. Sorry, we're slammed. Corporate merged three afterlives last quarter and nobody migrated the records properly. Okay! You qualify for reincarnation into a world of swords and sorcery, blah blah, adventure awaits, and you get one Divine Blessing. Most people take Infinite Mana or Sword Saint."

"What do *you* recommend?"

She blinked. Nobody had asked her that in several thousand years. "Honestly? Something that would've helped you last time."

Mike thought about Chad's whiteboard. About the HR meeting. About two weeks becoming a contract.

"I'd want to know how long things actually take," he said. "Exactly. So nobody can argue."

"Done!" She stamped the form before he could finish. Then she frowned. "Wait. I think I put that in the wrong field. That's not a combat blessing, that's a... utility passive."

"Is that bad?"

"Well, it'll be accurate. It just won't make anyone *listen* to you." She was already pressing a large red button. "Ticket closed! Have a blessed rebirth!"

The floor vanished. Mike fell, and the last thing he saw before the light took him was a glowing line of text hanging in the air in front of his eyes:

**\[Accurate Estimation\] acquired.**

**Estimated time until you regret this: 12 years, 0 months, 3 days.**
