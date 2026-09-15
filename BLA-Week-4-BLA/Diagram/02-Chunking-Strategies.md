# Chunking Strategies

```text
                    DOCUMENT
                       |
        +--------------+--------------+
        |              |              |
        v              v              v
    STANDARD      HIERARCHICAL      SEMANTIC
    CHUNKING        CHUNKING        CHUNKING
        |              |              |
 Fixed token      Small child      Group by
    size           chunks +         meaning
        |          larger parent       |
        v              v              v
 Simple and       Precision +       Topic-based
 predictable       more context      grouping
```

## Easy Way to Remember

- Standard = split by size
- Hierarchical = small and large chunks together
- Semantic = split by meaning
