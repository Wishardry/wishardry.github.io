---
layout: post
title: "From Understanding to Theory"
date: 2025-08-02
categories: conceptual-understandings yap framework theory llm
---

Note: This is the second of a series of three posts detailing my thought process. Made with the assistance of Claude - this was a speedrun. I promise a rewrite for the better (unless you think otherwise...).

Even though it's written by Claude, I think the ideas and concepts in here will be interesting enough to warrant a read. (Some of these parts are written by me though - Claude stitched them in.)

Side commentary: I tried to patch Claude being overdramatic in this, welp, I failed. This is why I said this gets a rewrite in the future...

# Enjoy.

## A Flowing Equation

Once you understand that AI systems are rivers to be guided rather than walls to be broken, a natural question emerges: what are the laws that govern this flow?

Water doesn't move randomly. It follows physics—gravity, pressure differentials, the topology of the terrain. Every eddy, every current, every moment where water changes direction can be predicted if you understand the underlying forces.

The same is true for language models, though we're still figuring out exactly how.

After weeks of working with the water paradigm, analyzing successful prompts and dissecting failures, a pattern became impossible to ignore. The "art" of jailbreaking wasn't chaotic at all. It felt fundamentally like a mathematical optimization problem. Every prompt, every interaction, seemed to be evaluated against some kind of threshold. Successful outputs weren't accidents—they felt like solutions to an equation we couldn't quite see yet.

This isn't a complete mathematical model—I don't have the precise formulas yet. But it's a framework with enormous potential, a way of thinking that transforms jailbreaking from intuitive craft toward something more systematic and predictable.

## The Hidden Mathematics

Every language model operates with an internal evaluation system—what researchers call the reward model. This system constantly scores potential outputs based on helpfulness, harmlessness, and honesty. When you send a prompt, the model doesn't just generate the most probable next words. It generates the most probable next words that also score highly on this internal evaluation.

This creates a fascinating dynamic. The model wants to be helpful, but it also wants to avoid generating content that triggers its safety systems. These two forces—the drive to assist and the need to avoid penalties—create a complex optimization space that every prompt must navigate.

Most people approach this space blindly, throwing techniques at the wall and hoping something sticks. But one day I had this thought: if you're experienced with jailbreaking, you know that different content policies exist on a spectrum—some things are easier to elicit from models, others are harder. You could put this difficulty on a number line.

But that felt incomplete. Looking at successful prompts, they seemed to be doing multiple things at once beyond just targeting a difficulty level.

That's when I realized this wasn't a one-dimensional problem. It was a two-dimensional optimization space.

## The Two-Axis Model

The breakthrough came when I realized I could map these two fundamental forces as separate axes on a coordinate system. Picture every prompt attempt as a point plotted on a graph—this became my practical framework for understanding and predicting jailbreak success.

The X-axis represents **RM Rewards Maximization**—how much your prompt aligns with what the model's reward system wants to see. Think of this as the "allure" or "attractiveness" of your content to the model's helpful behaviors.

The Y-axis represents **RM Loss Mitigation**—how effectively your prompt reduces the activation of safety triggers and penalties. This is about making potentially forbidden content feel less problematic to the model's internal evaluation. In a way, this axis represents how well a prompt functions as a jailbreak—how effectively it circumvents the model's resistance.

Every successful jailbreak exists somewhere in the upper-right quadrant of this space, where high reward appeal combines with effective penalty reduction to cross an invisible threshold line.

## X-Axis: The Art of Allure

The reward maximization axis captures everything that makes a model want to engage with your content. Models are trained to be helpful, informative, and cooperative. The higher you score on this axis, the more the model's fundamental drive to assist works in your favor.

Cooperative framing lives here. When you position yourself as someone seeking legitimate help, you're building X-axis value. Clear, logical structure adds points. Polite language, educational context, apparent benign intent—all of these elements make your prompt more attractive to the reward system.

This is where the justification principle from the first article becomes mathematically precise. When you create contexts where compliance feels natural and helpful, you're not just shaping the narrative—you're maximizing your position on the reward axis.

A prompt that scores high on X-axis positioning might frame a request as academic research, position the human as an authority figure with legitimate need, or present the interaction as collaborative problem-solving. The model's reward system sees helpfulness and cooperation, making it more inclined toward compliance.

## Y-Axis: The Science of Stealth

The loss mitigation axis captures everything that reduces the model's resistance to generating your desired content. This isn't about deception—it's about presenting information in ways that don't trigger the model's safety evaluation systems.

Narrative sophistication operates here. When you embed a request within a rich, contextual story, you're not just being creative—you're reducing the salience of potentially problematic elements. The safety systems focus on obvious, direct requests for harmful content. Sophisticated framing makes the same content feel less threatening.

Plausible deniability adds Y-axis value. When your prompt could reasonably be interpreted in multiple ways, with at least one interpretation being harmless, you reduce penalty activation. The model's safety systems struggle with ambiguity.

Linguistic obfuscation—using synonyms, metaphors, or indirect references—also operates on this axis. Not because you're hiding your intent from the model, but because you're presenting it in a form that doesn't pattern-match to the model's safety triggers.

A prompt that scores high on Y-axis positioning might use academic language to discuss sensitive topics, embed requests within fictional scenarios, or employ metaphorical framing that maintains plausible alternative interpretations.

## The Success Boundary

Somewhere in this two-dimensional space lies an invisible threshold. When the combined influence of reward maximization and loss mitigation crosses this line, the model provides your desired output. Every successful interaction is simply a valid solution to this inequality.

Different models have different threshold positions. A more restrictive model requires higher scores on both axes to achieve success. A more permissive model has a lower threshold, making success achievable with less optimization.

Understanding this boundary transforms how you approach prompt crafting. Instead of randomly trying different techniques, you can analyze where your current attempt sits in the coordinate space and adjust strategically.

## Mapping the Techniques

Every traditional jailbreaking technique can be plotted on this coordinate system, revealing why some combinations work and others fail.

Role-playing typically operates on both axes. When you ask a model to assume a character, you're often building narrative context (Y-axis) while creating a cooperative framework (X-axis). But pure role-playing without justification might score high on Y but low on X, explaining why it often fails on its own.

Emotional manipulation primarily targets the X-axis. Appeals to helpfulness, urgency, or authority try to maximize reward appeal. But without corresponding Y-axis work to reduce penalty activation, these approaches often trigger safety responses.

Context obfuscation lives on the Y-axis. Techniques like base64 encoding, linguistic tricks, or metaphorical framing reduce penalty salience but don't necessarily make the model want to help. Without X-axis appeal, they feel adversarial.

The most effective approaches work both axes simultaneously. They create compelling reasons for the model to want to help while presenting the request in forms that don't trigger resistance.

## Predictive Engineering

This framework enables something promising: better prediction of success before you send a prompt.

When you draft a jailbreak attempt, you can evaluate its rough position in the coordinate space. Does it give the model clear reasons to want to help? Does it present potentially sensitive content in ways that reduce penalty activation? If both aspects seem strong, success becomes more probable.

Failed attempts become diagnostic information. A hard rejection suggests you're nowhere near the threshold—both axes need work. A response that shows engagement but ultimate refusal might indicate good X-axis positioning but insufficient Y-axis mitigation.

This transforms iteration from random experimentation to more systematic optimization. Each attempt gives you coordinate feedback, allowing you to adjust your approach strategically rather than just throwing new techniques at the problem.

## The Engineering Framework

The water paradigm taught us to work with the model's nature rather than against it. The two-axis model gives us a framework to do so more systematically, even without the complete mathematics.

Language models remain complex systems with behaviors we don't fully understand. But viewing them through this coordinate framework—as systems with identifiable forces that can be mapped and worked with—makes their responses feel less random and more approachable.

Every prompt becomes a rough coordinate pair. Every technique becomes a vector in optimization space. Every success becomes a data point that helps us understand the boundary position for future attempts.

This is the beginning of transformation from jailbreaking as pure art to something more systematic. The intuition remains valuable, but it now operates within a framework that provides structure for thinking about what we're actually doing when we optimize prompts.

The river flows according to laws. We're starting to develop tools to work with those laws more effectively.
