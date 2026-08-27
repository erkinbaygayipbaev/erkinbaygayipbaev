### Erkinbay Gayipbaev

Founder of **Tariffs AI**. I build AI systems for Uzbekistan's customs and public sector — the kind where a wrong number costs someone real money, so the answer has to be verifiable, not just fluent.

Based in Nukus, Karakalpakstan. Software Engineering at Nukus State Technical University.

---

### What I'm building

**[Tariffs AI](https://github.com/erkinbaygayipbaev/tariffs-ai)** · [tariffs-ai-rag.vercel.app](https://tariffs-ai-rag.vercel.app)

Type a product description in plain Uzbek, get the TIF TN customs code, import duty and VAT.

The hard part isn't retrieval — it's being right. Language models confuse `0.2%` with `2.0%`, and a customs officer will not forgive that. So the model only answers *which code*; the rate itself is looked up in the official tariff table (1,845 records, decree ПҚ-3818) and corrected if the model disagreed.

- Hybrid retrieval: Vertex AI semantic search **and** a local keyword index. Semantic search alone returned nothing for the query "dori" (*medicine*) even though the word appears four times in record 3004.
- 407 of the 1,845 codes carry a duty that is not a flat percentage — `70% + $3 per cm³`, or `5% but no less than $0.10/kg`. Generic tariff calculators drop that second term. On a 2000 cm³ vehicle that understates the total payment by 35%.
- Cyrillic and Latin Uzbek normalise to the same search form, so `дори` and `dori` both hit.
- 52 evals gate every change.

`Next.js` · `Vertex AI (Gemini)` · `Firebase` · `Vercel`

---

### Shipped

| | |
|---|---|
| **Mo'ynoq District Government bot** | AI Telegram bot for the citizen-appeals office of Mo'ynoq district. Live since August 2026, 24/7 on Google Cloud with systemd auto-restart; the VM reaches Vertex AI through its own service scope, no key files on disk. |
| **[Dápter-Cloud](https://github.com/erkinbaygayipbaev/Dapter-Cloud)** | Debt-ledger SaaS for small shop owners. Multi-language, paid tier. |
| **Shumanay Digital Twin** | Digital twin of Shumanay district. |
| **[Advanced DSA Library](https://github.com/erkinbaygayipbaev/Advanced-DSA-Library-cpp)** | Complex data structures and algorithms in C++. |

---

### Background

IT Park Uzbekistan incubation · pitched at Demo Day and Investor Day.

Karakalpak (native) · Uzbek · Russian · English

📧 erkinbaygayipbaev@gmail.com
