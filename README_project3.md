# NER + Relation Extraction → Knowledge Graph

An end-to-end information extraction pipeline that turns unstructured text
into a queryable knowledge graph. A fine-tuned transformer identifies
entities, dependency-parse rules extract relations between them, and the
resulting triples are assembled into a graph you can query, traverse, and
visualize.

```
Raw text
   ↓  [DistilBERT token classification, fine-tuned on CoNLL-2003]
Entities  (PER / ORG / LOC / MISC)
   ↓  [spaCy dependency-parse SVO extraction]
Triples   (subject, relation, object)
   ↓  [NetworkX graph construction]
Knowledge Graph  — queryable, traversable, visualizable
```

## Motivation

NER on its own gives you a list of names. That's not knowledge — it's a word
list. The interesting problem is the second half: recovering how those