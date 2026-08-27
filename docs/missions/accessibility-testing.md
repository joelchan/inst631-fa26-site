Manual & Automated Accessibility Testing Mission

Pick a website to evaluate, and a screen reader to use. 
 
^todo-screenreader

!!! note "You already have a screen reader"

    **Mac:** VoiceOver is built in — ⌘F5 to toggle. **Windows:** Narrator is built in (Ctrl+Win+Enter), or install [NVDA](https://www.nvaccess.org/) free. **Android:** TalkBack, in Accessibility settings. **iPhone:** VoiceOver, same. You do not need to buy anything — JAWS is the paid one and you don't need it for this.


!!! warning "What you're doing, and what you're not"

    You are using the screen reader as **an instrument that exposes the page's underlying structure** — what the machine can and can't work out about this interface. You are *not* simulating the experience of being a screen reader user, and an hour with VoiceOver doesn't tell you what it's like to rely on one. Daily users are fast, run speech far quicker than you'll be able to follow, and have workarounds you don't. Keep your findings about the *page*.


## Part 1: Manual Testing

Identify 4-10 WCAG violations, and describe them. Take screenshots of the webpage/HTML code, if relevant, to help describe each violation. Explain which guideline is being violated, and how you can tell. 

!!! tip "You already did the first hour of this"

    In Week 10 you picked this page, picked a task, and drove it keyboard-only. **Use the same page and the same task here**, and bring that list with you — keyboard traps, lost focus, and surprising focus order are all WCAG violations, and they count toward your 4–10. The screen reader adds speech on top of navigation you already know.


Directions: Do a manual inspection of a specific webpage in two passes. **First, listen** — turn the screen reader on, stop looking at the screen, and try to complete an ordinary task on the page. **Then look at the code** — go back to the HTML and work out what caused each thing you noticed. The order matters: you're finding a symptom by ear, then locating its cause in the markup, which is how this is done in practice.

A screen reader is especially good at exposing:

- images with missing, useless, or wrong alt text ("image", "IMG_2049", or describing the wrong thing)
- form fields with no label, so you hear "edit text" and nothing else
- heading structure that's broken or fake — jumping h2 → h4, or bold text used where a heading belongs
- missing landmarks, so there's no way to skip to the main content
- link text that says nothing out of context — "click here", "read more", "learn more"
- focus order that jumps around the page — you'll hear yourself land somewhere that makes no sense
- ARIA that lies — a label or role that doesn't match what the control actually does

Note what is **not** on that list: whether the focus indicator is *visible*. A screen reader announces what has focus whether or not anything is drawn on the screen, so a missing or invisible focus ring (WCAG 2.4.7), focus hidden behind a sticky header (2.4.11), and an indicator too faint to spot (2.4.13) are all things this pass structurally cannot find. Those come from your keyboard hour, with your eyes open. Two instruments, different sensitivities — which is the same lesson Part 3 asks you to draw about manual versus automated.

Remember to share what webpage you picked, and what screen reader you used!

## Part 2: Automated Testing

Identify 3 violations that the tool identified. Take screenshots of the webpage/HTML code, if relevant, to help describe each potential violation. Share what the tool says is happening, and explain whether or not you think the tool is right. 

Directions: On that same webpage, use an automated tool to evaluate accessibility. Find potential WCAG violations according to those tools. 

Remember to share which automated tool you used!

## Part 3: Comparison

What similarities and differences did you find between the manual testing and automated testing? What did you find that the automated tool didn’t, and vice versa? 

