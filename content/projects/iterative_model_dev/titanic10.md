---
title: Building Interpretable Models
weight: 120
alwaysopen: false
lastmod: 2019-06-14
typora-root-url: ../../../static
---
#### Notebook: <a href="http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/TitanicN10.ipynb" target="_blank">Building an Interpretable Model</a>
#### Goals  
- Build two small, simple, yet accurate DecisionTrees for the Titanic data set
- Use Decision Trees to show how features are associated with survival rate

#### Results  

##### Reading the Decision Tree

- The left branch is always True, the right is always False.
- 'Master' is the title given to boys.
- Sex == 0 => male
- Sex == 1 => female
- Title_Master == 0 => title is not 'Master'
- 
  Title_Master == 1 => title is 'Master'   

 

![Tree1](/images/Tree1.png)

Interpreting the Above Tree

The captain's order was to give preference to women and children to board the life boats.  "Women" includes female children.  The two groups that had the highest survival were women and boys.  However for both groups, those from large families did not fare well.  Perhaps this is because family members stuck together and there was not room enough on the life boats for an entire large family.

![Tree2](/images/Tree2.png)

Interpreting the Above Tree

This tree was slightly or no better than the previous tree, however it shows the role of passenger class.  Men in 1st class had a survival rate of 42/119 = 35% whereas men in 2nd and 3rd class had a survival rate of 44/418 = 11%.  Women in 1st class or 2nd class had a survival rate of 161/170 = 95% whereas women in 3rd class from small families had a survival rate of 69/117 = 59% and from large families of 3/27 = 11%.

This is the last in the 10 part series on Iterative Model Developer with Scikit Learn.