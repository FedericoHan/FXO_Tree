#FXO_Tree

This notebook creates a tree to price a Currency Option as an example of forward and backward reasoning for
"Thinking Strategically" @ London Business School, taught by Professor David Myatt.

Namely, a tree is built with the _setup_parameters_() and _initialize_underlying_tree_() methods from 
the BinomialTree class, going from today to the expiry date.

Then, backward induction, starting from the final date begins with the _traverse_tree_() method, which
checks for payoffs and early exercise from N back to the present day.  



The implementation has some slight variations to use calendar dates 
and then fitting the tree branching to implied volatility from James Ma's excellent 'Python For Finance'.

Pricing of a European and American call USD/JPY Put, 8.15% vol, yields values of USD 106,080 and USD 112,593 respectively, versus professional pricers of USD 104,500 and USD 112,000.  
