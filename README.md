# RAG-API

Production-oriented Retrieval-Augmented Generation (RAG) platform built with .NET 8, PostgreSQL, pgvector, Redis and OpenAI.

## Problem

Organizations store valuable knowledge in documents, policies, manuals and operational procedures.

Traditional keyword search often fails when users do not know the exact wording used in documents.

This project demonstrates how AI-powered semantic retrieval can improve knowledge discovery while maintaining control over enterprise data.

## Key Features

* Document ingestion
* Chunking pipeline
* Embedding generation
* Vector search
* Hybrid search
* Metadata filtering
* Reranking
* Conversation history
* Audit logging

## Architecture

Client
↓
API Gateway
↓
RAG Service
↓
PostgreSQL + pgvector
↓
LLM Provider

## Technology Stack

* .NET 8
* ASP.NET Core
* PostgreSQL
* pgvector
* Redis
* Docker
* OpenAI

## Trade-offs

### Why PostgreSQL + pgvector?

Pros:

* Lower operational cost
* Single database
* Easy deployment

Cons:

* Lower scalability compared to dedicated vector databases

Decision:
Chosen because simplicity and maintainability outweighed hyperscale requirements.

### Why Hybrid Search?

Pros:

* Better recall
* Better retrieval quality

Cons:

* Increased implementation complexity

Decision:
Enterprise search quality is more important than implementation simplicity.

## Future Improvements

* Multi-tenant support
* Role-based document access
* Distributed embedding pipeline
* Local LLM support
