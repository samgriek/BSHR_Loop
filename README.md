# BSHR_Loop

Welcome to BSHR_Loop, a project that aims to automate human search behavior for addressing any information need in an arbitrarily large information domain. BSHR stands for Brainstorm, Search, Hypothesize, Refine, a technique that models "information foraging" in humans.

## Overview

BSHR_Loop uses Large Language Models (LLMs), a type of deep neural network based on the "transformer" architecture, to perform the following:

1. **Brainstorm**: Accept user queries or information problems of arbitrary size, length, and complexity. The LLM then brainstorms a list of search queries, ensuring a well-rounded search by employing information literacy and counterfactual queries.

2. **Search**: The brainstormed list of questions is used to search an information source, such as a search API, KB database, or KG. The search results are cached locally so that the system knows what it has already seen. This is crucial for the BSHR loop to know when available information has been exhausted.

3. **Hypothesize**: The LLM "reads" all the searched materials and formulates an early hypothesis based on the user's information needs. It does so by "taking notes", a function that LLMs excel at. The hypothesis is recorded with citations.

4. **Refine**: This step is more of a recursion. The next loop performs an "informed search" rather than a "naive search". After the first pass of searched material and hypothesis, the next pass can use this information to write better search queries and refine the hypotheses.

At the end of each loop, a complete function is written where the LLM decides if the information need has been satisficed, a specific term from information and library science. The decision is based on the amount and quality of evidence supporting the hypothesis and whether or not new information is available, or if the information domain has been exhausted.

## Theory

In this section, we delve into the key concepts from library and information science that underpin the BSHR_Loop project. Understanding these terms will provide a deeper insight into the project's design and functionality.

**Information Foraging**: This term is inspired by the concept of food foraging in animals. In the context of information science, it refers to the process of seeking, gathering, and consuming information. Just as animals forage for food, humans forage for information in their environment. The BSHR_Loop project models this behavior, enabling the system to navigate through vast information domains, identify valuable information, and make decisions based on the gathered data.

**Information Literacy**: Information literacy is the ability to identify, locate, evaluate, and effectively use information. It's a critical skill in today's digital age where information is abundant. In the BSHR_Loop, the LLM employs information literacy to brainstorm a broad list of queries, ensuring a comprehensive and well-rounded search. It also uses this skill to evaluate the quality of the information found and to refine the search queries and hypotheses.

**Satisficing**: A term coined by Herbert Simon, a Nobel laureate in economics, satisficing is a decision-making strategy that aims for a satisfactory or adequate result, rather than the optimal solution. In the context of information science, it refers to the point at which enough information has been gathered to meet the user's needs. In the BSHR_Loop, the LLM uses a variety of factors to determine if the information need has been satisficed. These factors include the amount and quality of evidence supporting the hypothesis and whether or not new information is available, or if the information domain has been exhausted.

**Information Needs**: This term refers to the desire to obtain information to satisfy a conscious or unconscious need. In essence, all queries are expressions of information needs. Information needs can vary greatly in complexity, from simple factual queries to more complex and ambiguous questions. In the BSHR_Loop, the LLM accepts user queries or information problems of arbitrary size, length, and complexity, and uses these as the starting point for the Brainstorm, Search, Hypothesize, Refine process. The ultimate goal of the BSHR_Loop is to satisfice these information needs by gathering, processing, and presenting relevant information.

## Use Cases

The BSHR_Loop is designed to be versatile and adaptable, capable of addressing a wide range of information needs across various domains. Here are some examples of how it can be implemented:

**Business Data Lake**: In the context of a business data lake, the BSHR_Loop can be used to navigate through vast amounts of unstructured and structured data. It can help answer complex business queries, identify trends, and provide insights that can drive decision-making. For instance, it can help a business analyst understand the impact of a particular marketing campaign by brainstorming relevant queries, searching through the data lake, formulating hypotheses, and refining these hypotheses based on the evidence gathered.

**Internet Search**: The BSHR_Loop can be used to enhance the effectiveness of internet search. It can help users navigate through the vast amount of information available online and find the most relevant and reliable sources. For example, a student researching a complex topic can use the BSHR_Loop to generate a list of search queries, find relevant sources, formulate an initial understanding of the topic, and refine this understanding as more information is gathered.

**University Library System**: In a university library system, the BSHR_Loop can be used to help students and researchers find the information they need. It can generate a list of search queries based on the user's information needs, search through the library's resources, formulate a hypothesis, and refine this hypothesis as more information is gathered. This can be particularly useful for literature reviews or research projects.

**Personal Archive**: The BSHR_Loop can also be used to navigate through personal archives, such as a collection of digital photos, documents, or emails. It can help users find specific items in their archive based on their information needs. For example, a user looking for all photos from a particular event can use the BSHR_Loop to generate search queries, find relevant photos, and refine the search as needed.