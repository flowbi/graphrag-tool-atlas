# GraphRAG Tool Atlas

The GraphRAG market is easier to compare when each product is described by what it consumes and what it produces. A tool that derives semantic definitions, a loader that writes business facts, and an application that answers questions all contribute different outputs—even when all three are described as knowledge-graph software.

This directory uses **one alphabetical comparison matrix** across frameworks, enterprise products, graph engines, and supporting tools. It contains 37 documented offerings, with primary-source links on their names.

**Research snapshot: 5 November 2026.** Descriptions are research summaries rather than tested integrations or performance scores. “GraphRAG” refers to the broader graph-assisted retrieval family; Microsoft GraphRAG is one particular implementation.

## The output vocabulary

| Output | What it means here | Concrete example |
| --- | --- | --- |
| Semantic model | Definitions of concepts, attributes, relationship types, identifiers, and source mappings | What a device is, what `INSTALLED_AT` means, and which source fields identify it |
| Ontology | Formal domain definitions and potentially logical axioms | Device classes, property meanings, and inference semantics |
| Populated knowledge graph | Identifiable entities, facts/assertions, relationships, and evidence | Device D-18 is installed at site S-9, according to record R-4 |
| Retrieved context | Evidence selected for a question | Relevant paths, records, passages, or summaries |
| Generated response | The answer composed from available context | A device-impact explanation with supporting references |

These are functional distinctions, not requirements for separate storage. Semantic definitions can themselves form a graph, and a knowledge graph can include both ontology and instance data. Producing a semantic model alone does not populate business facts. [W3C RDF Schema](https://www.w3.org/TR/rdf-schema/), [W3C OWL primer](https://www.w3.org/TR/owl2-primer/)

## Alphabetical software directory

Read **product form** alongside **output**. Database engines, modeling tools, retrieval libraries, and evaluation services are complementary roles rather than equivalent alternatives. Inputs are representative of the documented approach, not exhaustive connector lists.

| Tool / primary evidence | Product form | Starting input | Principal output | Dependency / scope note |
| --- | --- | --- | --- | --- |
| [Amazon Bedrock Knowledge Bases GraphRAG](https://docs.aws.amazon.com/bedrock/latest/userguide/knowledge-base-build-graphs.html) | Managed service | Documents in supported sources | Constructed graph and graph-enhanced answer context | Uses Neptune Analytics; inspect S3 and customization limits |
| [Amazon Neptune Database](https://aws.amazon.com/neptune/graph-and-ai/) | Graph service family | Graph data | Stored/queryable graph and analytical access | Database and Analytics are distinct services |
| [ArangoDB](https://arango.ai/) | Multi-model platform | Graph/document/vector data | Queryable connected data and search results | Distinguish database and broader platform suite |
| [AWS GraphRAG Toolkit](https://github.com/awslabs/graphrag-toolkit) | Developer toolkit | Documents or an existing graph | Lexical graphs or graph-grounded retrieval | Component, graph store, vector store, and model choices |
| [Azure Cosmos DB for Apache Gremlin](https://learn.microsoft.com/en-us/azure/cosmos-db/graph/gremlin-support) | Graph service | Graph data | Gremlin traversal results | API compatibility and partitioning matter |
| [cognee](https://github.com/topoteretes/cognee) | AI memory framework | Knowledge inputs | Persistent context and retrieval | Inspect configured graph/vector backends |
| [DeepEval](https://deepeval.com/) | Supporting evaluation | Test cases and application outputs | Quality metrics and test results | Define graph-specific assertions separately |
| [Docling](https://docling-project.github.io/docling/) | Supporting parser | Documents | Structured document content and chunks | Parsing does not establish domain meaning or truth |
| [FalkorDB](https://www.falkordb.com/graphrag/) | Graph database | Nodes and edges | Stored graph and traversal results | Runtime for its SDK/Server ecosystem |
| [FalkorDB GraphRAG-SDK](https://github.com/FalkorDB/GraphRAG-SDK) | Application SDK | Structured/unstructured inputs | Ontology proposals, populated graphs, and retrieval | Separate SDK, Server, and database responsibilities |
| [fast-graphrag](https://github.com/circlemind-ai/fast-graphrag) | Retrieval framework | Domain-guided document knowledge | Graph exploration and answer context | Personalized PageRank; distinct from Microsoft's fast method |
| [Flow.BI](https://flow.bi/solutions/flow-bi-for-knowledge-graphs/) | Semantic-model discovery | Metadata and profiled enterprise data | Concept definitions and source mappings | Separate ekg/doc-ekg loaders populate and enrich the graph |
| [Google Spanner Graph](https://docs.cloud.google.com/spanner/docs/graph/overview) | Graph/relational engine | Relational records and graph schema | Queryable property graph | Edition, dialect, and integration configuration apply |
| [Graphiti](https://github.com/getzep/graphiti) | Temporal memory framework | Events, episodes, and changing facts | Temporal knowledge graph and retrieved context | Define current versus historical query behavior |
| [Graphwise GraphRAG](https://help.graphwise.ai/gwp26-1/en/graphrag.html) | Semantic application platform | Semantic context, graphs, and documents | Graph-grounded conversational responses | Graph Modeling and GraphDB contribute separate roles |
| [HippoRAG](https://github.com/OSU-NLP-Group/HippoRAG) | Research framework | External document knowledge | Graph-assisted retrieval using PageRank | Reproduce the selected project generation |
| [KAG](https://github.com/OpenSPG/KAG) | Domain reasoning framework | Domain knowledge and schema | Aligned graph knowledge and reasoning/retrieval | OpenSPG ecosystem; assess schema and language coverage |
| [LangChain graph integrations](https://docs.langchain.com/oss/python/integrations/graphs/neo4j_cypher) | Application framework components | Existing graph or constructed knowledge | Graph query access and composed workflows | Application defines extraction, retrieval, and access rules |
| [Langfuse](https://langfuse.com/docs) | Supporting observability | Application traces and evaluation data | Runtime, prompt, cost, and quality observations | Instrument graph queries and evidence selection |
| [LightRAG](https://github.com/HKUDS/LightRAG) | Graph/vector RAG framework | Documents | Entity/relationship index and retrieved context | Query-mode semantics differ from other implementations |
| [LlamaIndex PropertyGraphIndex](https://developers.llamaindex.ai/python/framework/module_guides/indexing/lpg_index_guide/) | Developer framework | Documents or property graph data | Extracted paths, graph indexes, and query results | Selected extractors, graph store, and retrievers determine behavior |
| [Memgraph](https://memgraph.com/graphrag) | Graph database ecosystem | Connected records | Graph storage and graph-backed queries | Check the specific GraphRAG integration |
| [metaphactory](https://metaphacts.com/solutions/products/metaphactory) | Semantic application platform | Domain models and enterprise knowledge | Semantic models and conversational graph applications | NL-to-SPARQL and unstructured RAG services differ |
| [Microsoft GraphRAG](https://github.com/microsoft/graphrag) | Research pipeline | Text corpus | Extracted graph, community reports, and search context | Repository states maintenance mode; multiple query modes |
| [nano-graphrag](https://github.com/gusye1234/nano-graphrag) | Compact framework | Text corpus | GraphRAG indexes and retrieval | Assess storage choices and maintenance suitability |
| [Neo4j / Aura](https://neo4j.com/docs/neo4j-graphrag-python/current/) | Graph database family | Property graph data | Stored graph and Cypher query results | Edition, version, schema, and indexes matter |
| [Neo4j GraphRAG for Python](https://neo4j.com/docs/neo4j-graphrag-python/current/) | GraphRAG library | Neo4j graph and/or construction inputs | Built graph, retrieved evidence, and generated responses | Requires supported Neo4j and configured models |
| [Neo4j LLM Knowledge Graph Builder](https://neo4j.com/developer/genai-ecosystem/llm-graph-builder/) | Graph-building application | Unstructured documents | Entity/relationship graph linked to source chunks | Inspect extraction schema, identity merging, and evidence |
| [Phoenix](https://arize.com/phoenix/) | Supporting observability | Application traces and test outputs | Evaluation results and runtime traces | General AI tooling; add graph-specific instrumentation |
| [Protégé / WebProtégé](https://protege.stanford.edu/) | Ontology editor | Domain vocabulary and axioms | Formal ontology definitions | Produces semantics; not an automatic instance loader |
| [PuppyGraph](https://www.puppygraph.com/) | Graph query engine | Relational data and mappings | Graph-query access over existing records | Semantic discovery and answer generation remain separate |
| [Ragas](https://docs.ragas.io/en/stable/) | Supporting evaluation | Retrieved context and responses | Retrieval and answer metrics | Pair generic scores with known graph facts |
| [Senzing](https://senzing.com/) | Supporting identity resolution | Fragmented entity records | Resolved identities and relationships | Entity resolution differs from defining concept types |
| [Stardog Voicebox](https://docs.stardog.com/voicebox/) | Conversational application | Enterprise graph context and documents | Graph queries, analysis, and attributed responses | Verify which answer path supplied the evidence |
| [TigerGraph GraphRAG](https://www.tigergraph.com/graphrag/) | Enterprise graph/AI offering | Connected operational data | Graph/vector retrieval and application context | Specify database, integration, and application scope |
| [TopBraid EDG](https://ww2.topquadrant.com/release-note/9-0/) | Semantic governance platform | Models, vocabulary, and content | Semantic assets and GraphRAG-enabling access | Check release, ingestion, and answering components |
| [Unstructured](https://docs.unstructured.io/) | Supporting parser/extractor | Documents | Parsed content and structured fields | Retain source references through downstream ingestion |

## Read the same directory through four market views

| Market view | The distinction to inspect | Examples in the matrix |
| --- | --- | --- |
| Knowledge foundations | Semantic definitions versus populated entity facts | Flow.BI, Protégé, semantic platforms, graph builders |
| Retrieval implementations | Query generation, traversal, graph exploration, or community search | Neo4j GraphRAG, fast-graphrag, HippoRAG, Microsoft GraphRAG |
| Application delivery | Developer components versus packaged or managed services | LlamaIndex, LangChain, AWS Toolkit, Bedrock Knowledge Bases, enterprise assistants |
| Production infrastructure | Stored graph, query access, preparation, and measurable quality | Graph engines, parsers, tracing, and evaluation tools |

These are reading aids, not exclusive categories. A vendor can span several outputs without every component having the same role.

## Keep related products separate

| Names that overlap | Actual distinction |
| --- | --- |
| Microsoft GraphRAG and the wider GraphRAG market | One research implementation within a broader architectural family |
| Microsoft's FastGraphRAG and Circlemind fast-graphrag | An indexing method versus an independent project |
| AWS GraphRAG Toolkit and Bedrock Knowledge Bases GraphRAG | Open-source components versus a managed service |
| Neo4j database, GraphRAG library, and LLM Knowledge Graph Builder | Runtime, developer package, and construction application |
| FalkorDB database, GraphRAG-SDK, and GraphRAG Server | Engine, programmable toolkit, and packaged delivery |
| Flow.BI, flowbi/ekg, and flowbi/doc-ekg | Semantic derivation, structured graph loading, and document enrichment |

Graphiti and cognee emphasize persistent context and memory. They should be assessed on their own temporal and retrieval behavior rather than assumed to implement a community-summary pipeline. An orchestration graph describing agent steps is also different from a graph of domain knowledge used as evidence.

## Platform choices do not establish retrieval compatibility

Two tools may both name a graph database while expecting different schemas, source-chunk links, embeddings, or indexes. A graph engine may also expose relational data without copying all records into a separate store. In either case, define the data and evidence contracts before claiming the components form a working stack.

For example, an equipment-impact query might require device identities, installation records, component versions, and manual passages. Test each connection and its provenance. A relevant paragraph alone does not establish which devices are affected; a relationship path alone may not explain the required action.

## What this landscape does—and does not—establish

The source links support each product's described role. They do not establish universal accuracy, complete connector coverage, or a guarantee that graph-backed answers are grounded. Compare semantic meaning, identity, evidence paths, access control, freshness, and answer support on the same workload.

Use release-specific documentation for licensing, lifecycle, service regions, and dependencies. GraphDB and Stardog also supply graph storage within their wider ecosystems. This directory is broad public-tool coverage rather than a registry of every private accelerator.
