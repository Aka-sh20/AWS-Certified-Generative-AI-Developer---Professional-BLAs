# Reflection – Responsive and Resilient Generative AI Systems

This topic helped me understand the difference between an application that only works and an application that works well for real users.

Streaming showed me that user experience can improve even when total model generation time is similar because users can start reading earlier. I also learned that RAG performance depends on retrieval, filtering, and query preparation before the Foundation Model is called.

The resilience section was especially practical. Exponential backoff and jitter showed why a temporary failure should not cause immediate repeated retries. Connection pooling also showed that smaller infrastructure decisions around the model can improve efficiency.

Cross-Region Inference connected the reliability topic with available model capacity across supported AWS Regions.

My main takeaway is that responsiveness and resilience are properties of the complete system, not just the Foundation Model.
