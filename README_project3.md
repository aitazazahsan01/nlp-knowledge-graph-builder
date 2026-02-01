# NER + Relation Extraction → Knowledge Graph

An end-to-end information extraction pipeline that turns unstructured text
into a queryable knowledge graph. A fine-tuned transformer identifies
entities, dependency-parse rules extract relations between them, and the
resulting triples are assembled into a graph you can query, traverse, and
visualize.

```
Raw text
   ↓  [DistilBERT token classification, fine-tuned on CoNLL-2003]