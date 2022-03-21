# Distributed-Algorithms-for-Graph-Embeddings_Postgraduate-Thesis

Due to the continuously tendency to model domains in a network format,
network representation learning (NRL) is a field where a lot of research has
been carried out the recent years. Programmatically, a network is preserved
in an adjacency matrix that preserves the neighbors for each network’s node.
The size of the adjacency matrix is N×N, where N the number of nodes
in a network. For large networks, utilizing the vectors of the network’s nodes
preserved by the adjacency matrix is unfeasible in order to train machine
learning models to solve various network analytic tasks. The reason is the
size of the vectors, which for large networks is so big that makes practically
the training of the machine learning models unfeasible time-wise. The
objective of NRL is to map the original representation space of a network
(adjacency matrix) to a latent low-dimensional representation. The characteristics
of the new node vectors (node embeddings) are 1) the vectors’ size is
d, where d<<N, making the training of machine learning models time-wise
feasible and 2) the vectors try to capture as much as possible characteristics
of the original network to make the node embeddings as efficient as possible
in regard to the machine learning models training. A lot of NRL methods
have been developed and presented in the literature, which doesn’t respect
the scaling fact though, making them inapplicable in large networks. In 2018,
Zhang and his colleagues presented RandNE, “A novel and simple billion-
scale network embedding method based on high-order proximity preserved
random projection” (https://arxiv.org/pdf/1805.02396.pdf). RandNE showed exceptional time-wise performance,
but the provided implementation by (https://arxiv.org/pdf/1805.02396.pdf) is 1) centralized and 2) was tested
on small networks. Consequently, the objective of this thesis is the develop a
distributed version of the RandNE method utilizing the Apache Spark framework,
and examine its time-wise behavior. The implementation is available at (https://github.com/Tourgito/RandNE_Distributed).
The results showed that the provided implementation produces feasible execution times on large networks. In case of a network
with 334.863 nodes and 925.872 edges, a few minutes were enough in order the
implementation to be executed. Except from the main objective of this thesis,
this thesis is also a great entry-point for someone who is unfamiliar with the
NRL field, since it covers fundamental concepts, notations and definitions of
the field, as well as important NRL methods that have been developed in the
literature.
