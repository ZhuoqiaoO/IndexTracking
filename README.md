Replicating Portfolio with Cardinality and Buy-in Constraints

One portfolio construction problem is index tracking, where a portfolio is constructed to generate return similar to a certain index without purchasing all instruments in that index. This can be turned into an optimization problem, where the objective is to find the linear regression coefficients that minimize the tracking error between portfolio return and index return (here the l-1 norm -- maximum absolute error is used) and with budget constraints (budgets can not exceed certain amount), transaction costs constraints (transaction cost limited to certain percentage of budget, and constraints on the upperbound and lowerbound of the number of non-zero positions. The objective and constraints of such problem can be linearized and transformed into a mixed integer programming problem with objective being a linear regression problem. 

In this project I replicated Dow Jones index using R with the Portfolio Safeguard (PSG) packages. The in-sample data time period is from August 1, 2013 to August 31, 2023, where end of day adjusted prices data are pulled from Yahoo Finance. Not all data were available, in particular the data for the stock DOW is replaced by data of Dow Jones index ETF for the set time period. The setting is that non-zero positions limited to no more than 20 and budget constraint limited to 3000. With these parameters the problem is formulated and solved by PSG, and a graph is contructed to compare Dow Jones index returns with replicated portfolio return, result is as follow: 

![AltText]([ZhuoqiaoO/IndexTracking/TrackingComparison.jpeg](https://github.com/ZhuoqiaoO/IndexTracking/blob/4c189e8ebc5278e29d37274e4dc609d477102b85/Tracking%20Comparison.jpeg))



Reference: https://uryasev.ams.stonybrook.edu/index.php/research/testproblems/financial_engineering/case-study-portfolio-replication-with-cardinality-and-buyin-constraints/
