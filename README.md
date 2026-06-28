# Agricultural-Expert-System
A domain-specific question-answering system for Egyptian farmers built on a manually curated knowledge base covering 90+ crops, enhanced with a local LLM (Aya) for natural language understanding.


# Agricultural Expert System with LLM Enhancement

A domain-specific question-answering system designed to assist Egyptian farmers with crop management, disease diagnosis, and agricultural guidance — built as part of a graduation project.

---

## Project Overview
Traditional expert systems rely on strict rule-based matching which fails when users phrase questions informally or use dialect variations. This system solves that by combining a structured agricultural knowledge base with a local LLM layer that understands natural language queries in Egyptian Arabic and delivers clear, accessible responses.

---

## Knowledge Base
- **Built entirely from scratch** — manually researched, structured, and curated
- **90+ crops** covered
- **60+ parameters per crop** including planting seasons, irrigation methods, fertilization schedules, disease identification, pest control, harvesting guidelines, and market information
- Stored as structured JSON for efficient retrieval

---

## System Architecture
User Question (Arabic)

↓

Question Map — maps informal phrasing to knowledge fields

↓

Prompt Builder — injects question + knowledge base into LLM prompt

↓

Aya LLM (local) — understands query intent and generates response

↓

Answer in Egyptian Arabic

---

## Why LLM Enhancement
A pure rule-based expert system would fail on:
- Informal or dialect phrasing — "ازاي ازرع الطماطم" vs "كيف أزرع الطماطم"
- Combined questions — asking about planting and selling in one query
- Ambiguous intent — questions that don't map directly to a single data field

The LLM layer handles all of these by understanding intent before querying the knowledge base.

---

## Local LLM Setup
This project uses **Aya by Cohere** running locally via **Ollama** — no API key or internet connection required.

To run locally:
1. Download [Ollama](https://ollama.com)
2. Run `ollama pull aya` in terminal
3. Run all notebook cells

---

## Sample Outputs

**Question:** ازاي ازرع الطماطم وابيعها؟
**Answer:** detailed Arabic response covering planting seasons, irrigation, harvesting, and market tips

**Question:** ايه هي الامراض الي ممكن تقابل البطاطس؟
**Answer:** detailed Arabic response covering diseases, symptoms, prevention, and treatment

---

## Libraries Used
- requests
- json
