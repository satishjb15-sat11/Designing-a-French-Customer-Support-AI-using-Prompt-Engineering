# French Customer Support AI (Prompt Engineering Project)  

Prompt‑engineered French AI assistant for professional customer communication.  

## Overview

This project shows how prompt engineering can be used to design a reliable multilingual AI assistant for customer support.  
The focus is not on **coding**, but on prompt design, iteration, and output quality control.  

The assistant’s job: convert English customer messages into professional, polite French that fits real customer support scenarios.  

## Problem

Customer support teams often receive English messages that are emotional, unclear, or informal.  
Simple translation tools convert them directly into French, which often becomes:  
- Robotic  
- Impolite or too blunt  
- Not suitable for professional support conversations  

The goal is to convert English messages into French that is:  
- Polite  
- Professional  
- Clear  
- At B1–B2 French level  
while keeping the original meaning.  

**Raw problem example**  
English message:  
> “I have not received my order yet.”  

Naive translation:  
> “Je n’ai pas reçu ma commande.”  

Issues:  
- Too literal  
- Lacks politeness  
- No customer‑support tone  

## Prompt Design Strategy

To solve this, role‑based and constraint‑based prompting is used:  

- **Role assignment**: Set the AI as a “French customer support agent” / “professional French customer support assistant”.  
- **Tone constraints**: Ask explicitly for polite, professional, calm French, even if the English message is emotional.  
- **Language level**: Specify “simple, natural French (B1–B2 level)”.  
- **Output boundary**: “Output only the French message; no explanations.”  

## Prompt Iteration Log (Simplified)
This is a simplified view of how the prompt evolved.  

### v1 – Naive idea
“I created a French translator prompt.”  

Issue:  
- Only generic translation, no control over tone or context.  
- Output can feel rude or robotic.  

### v2 – Role + basic instruction

Concept prompt:  

> You are a French customer support agent.  
> Translate the following English message into polite French.  

Improvement:  
- Tone improves a bit.  

Issue:  
- Tone and level still inconsistent.  
- Instructions are still vague.  

### v3 – Final structured prompt

Final prompt:  
> You are a professional French customer support assistant.  
  
> Instructions:  
> - Rewrite the given English message into clear, polite, and professional French.  
> - Use simple and natural French (B1–B2 level).  
> - Preserve the original meaning.  
> - Do not add explanations or answers.  
> - Output only the French message.  
  
> English message:  
> “I have not received my order yet.”  

Final output:  

> “Je n’ai pas encore reçu ma commande.  
> Pourriez‑vous m’indiquer son statut, s’il vous plaît ?”  

Here:  
- Politeness is added.  
- Professional support tone is clear.  
- The original meaning is preserved.  
- An extra helpful sentence makes it sound like real support communication.

## Why This Is Prompt Engineering

This project does more than “just translate”: it designs a domain‑specific, tone‑aware AI assistant using prompts.  

It demonstrates:  
- Clear, constraint‑based instructions  
- Role‑based behavior design (customer support agent)  
- Control over tone and language level  
- Iterative refinement from a generic translator to a professional assistant  

The value comes from the prompt structure, iteration, and reasoning, not from complex code.
