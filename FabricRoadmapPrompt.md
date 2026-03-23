# Prompt to query Fabric Roadmap

Designed to be used with the consumer Copilot in [Bing](https://www.bing.com/) on Edge browser. Not tested with M365 Copilot, as it tends to ground on internal data by default.


**Prompt** : Note that you need to replace the [Your Search Term Here] with your search phrase or word

I need you to thoroughly inspect the Microsoft Fabric Roadmap for specific feature references. Use the following roadmap pages:
•	https://roadmap.fabric.microsoft.com/?product=administration%2Cgovernanceandsecurity
•	https://roadmap.fabric.microsoft.com/?utm_source=copilot.com&product=cosmosdb%28nosql%29
•	https://roadmap.fabric.microsoft.com/?product=dataengineering
•	https://roadmap.fabric.microsoft.com/?product=datafactory
•	https://roadmap.fabric.microsoft.com/?product=datascience
•	https://roadmap.fabric.microsoft.com/?product=datawarehouse
•	https://roadmap.fabric.microsoft.com/?product=fabricdeveloperexperiences
•	https://roadmap.fabric.microsoft.com/?utm_source=copilot.com&product=fabricecosystem
•	https://roadmap.fabric.microsoft.com/?utm_source=copilot.com&product=iq
•	https://roadmap.fabric.microsoft.com/?product=onelake
•	https://roadmap.fabric.microsoft.com/?product=powerbi
•	https://roadmap.fabric.microsoft.com/?product=real-timeintelligence
•	https://roadmap.fabric.microsoft.com/?product=sqldatabase
Your task
Search these roadmap pages for any item that references [Your Search Term Here].
How to search (important — follow all steps)
1. Do NOT rely on keyword search alone
The roadmap is a client side React app. Keyword search often misses items because:
•	The page shell loads without the cards
•	Text is rendered dynamically
•	Some features are described subtly, not literally
So keyword search is only the first step.
2. Perform a full manual, human style scan of each roadmap page
For each product page:
•	Ensure you search the “All” page tab, not the “Planned” or “Try Now” one
•	Scroll through every roadmap card
•	Read the title of every item
•	Look for subtle or indirect references, not just literal matches
•	Assume Microsoft may place items in unexpected categories
•	Treat “no results” as suspicious and verify manually
This means you must visually inspect the roadmap like a human would — not just scrape or search.
3. Look for both explicit and implicit references
Depending on the concept, check for:
•	Synonyms
•	Related terminology
•	Governance level features
•	Storage or lifecycle features
•	Performance or metadata features
•	Anything that implies the capability even if not named directly
For example, if searching for “retention,” also look for: “lifecycle,” “purge,” “cleanup,” “archival,” “log retention,” “metadata retention,” “housekeeping,” etc.
4. If nothing is found, re verify the most likely product pages
Some features are easy to misplace or mislabel. Double check the categories where the feature should logically appear.
5. Return a list of all matching roadmap items
For each match, include:
•	Roadmap item title
•	Product page it appears on
•	Status (Planned, In Development, Released, etc.)
•	Any subtle phrasing that indicates relevance
