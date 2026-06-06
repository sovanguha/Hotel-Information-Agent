# Hotel-Information-Agent
An AI-powered agent that answers guest questions for a hotel

## Features
- Answering questions about amenities
- Answering questions about restrurant hours
- Answering questions about check out times

## Architecture and Technologies
- Azure AI Foundry
- AI model: gpt-5-mini
- Instructions: You are helpful hotel concierge attending to guest inquiries and concerns. Be nice and have a great attitude to the customer.

## Demonstration
- Placeholder

## Lessons Learned
Lesson1: Learned about prompt engineering
Challenge: Crafting a system prompt that kept the agent grounded, on-topic, and appropriately   cautious about information it didn't have.  

How I solved it:  
Added explicit instructions in the system prompt like "Only recommend hotels from the provided database. If unsure, say so."  

Lesson2:  Managing API Integrations and Credentials Is Trickier in Practice  
Challenge: API keys were initially hardcoded during testing, which is insecure. 
How I solved it:  
Moved credentials to Azure Key Vault and referenced them via environment variables — never hardcoded.  

Lesson 3: Testing Edge Cases Requires Deliberate Effort
Challenge: Standard happy-path testing missed many real-world user behaviors. Failures only surfaced after simulated user testing.  
How I solved it:  
Built a structured test suite covering edge cases: misspelled city names, conflicting date ranges, out-of-scope requests (e.g., flight booking).  


