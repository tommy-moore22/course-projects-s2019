# Alex Mikes Project Proposal

I propose to create a software package that analyzes data from a design repository and uses it to create functional representations of components, with the eventual goal of automating the functional modeling process. This software will analyze the combinations of components and function-flow that are found in the products in the design repository, and create association rules based on the results. The association rules will be used to determine the most likely combinations of component and function-flow so that functional representations can be automatically generated for a given set of constituent components in a new product. 

The software will generate the functional representations based on some percentage threshold of statistical significance from one of the measures of association, most likely confidence. The process will be verified with case studies that calculate the accuracy of the data mining results by comparing them with the known component and function-flow combinations for various products. The accuracy will be determined by categorizing the ability of the data mining to match the actual functional representation. 

This process is something that I have done using a Python library to find the association rule results, and then I manually completed the thresholding, functional representations, and matching verification in Excel. Using Python, I plan on automating the same process but in a robust and expandable way that saves time and increases accuracy. The library I have been using to find the association rules is called `Apyori`, and I plan on continuing to use that for calculating association rules.

The design repository is a PostgreSQL database, and I would like to be able to query from within Python to import directly to Python data structures. I plan to use `psycopg`, which is the most popular library for interfacing Python with a PostgreSQL database.

The association rules are learned from a dataset, and in previous research, I compared the accuracy of the automated functional representations based on which data set was used for learning. With the proposal of automating this process, it would be feasible to optimize the dataset used for data mining based on some known similarities between the product for which the functional representation is being automated and the products from which the association rules are being learned. 

Without fully knowing how difficult any of this will be, if I am able to complete all of these tasks within a reasonable amount of time then I will set a stretch goal of using some sort of library (e.g. `PyGraphviz`) to generate visual functional representations. Because this is not a necessary part of the research but a potentially helpful tool for creating visuals, it is not crucial that it be completed.

This software will be used by myself and my fellow researchers who are working on automating functional modeling. 

In summary, I propose that I will write software that will:

1. Query a design repository in a PostgreSQL database within Python and store the results into Python data structures

2. Use association rules to find the prevalence of combinations of components and function-flow.

3. Apply a threshold of the top XX% of results for each component and call that the automatically generated functional representation for that component.

4. Compare the results of the automatically generated functional representation with the known functional representation and quantify the accuracy of the dataset that was used for data mining.

5. Compare the results of various datasets and optimize which is used for a given situation.

6. Stretch goal: Develop a visual of the automated functional representation
