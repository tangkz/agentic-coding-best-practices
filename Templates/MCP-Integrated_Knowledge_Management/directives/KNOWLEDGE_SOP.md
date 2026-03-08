# KNOWLEDGE SOP: [Topic/Domain]

## 1. Information Domain
Define the scope of knowledge being managed.
- **Source:** [e.g., API documentation, internal codebase]
- **Target Index:** [e.g., Pinecone/Supabase 'docs' table]

## 2. Extraction & Ingestion
- [ ] Read content from Source (Layer 1).
- [ ] Clean and chunk data for embedding.

## 3. Storage & Routing (Layer 3)
Define the scripts for indexing.
- `execution/upsert_to_vector.py`: Handles embedding and DB storage.
- `execution/query_mcp.py`: Verifies retrieval accuracy.

## 4. Quality Assurance
- [ ] Semantic consistency check.
- [ ] No duplicate context in top-K results.
- [ ] Update `.agent/skills/` if new patterns emerge.

## 5. Self-Annealing Triggers
Identify when retrieval is hallucinations or outdated.
- Trigger: Low cosine similarity score -> Action: Re-index domain with new chunking strategy.
