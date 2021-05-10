# Labs-Learnings


Q1.Comment the line option("inferSchema", "true") and run your program again. 
(Q1) What is the type of the attributes time and bytes this time? Why?
Answer : Time and Bytes are of datatype String.
The main reason  is default datatype after Split is String. And also, InferSchema is commented out. 
 Therefore, by default, it is populated as String Datatype.

(B): Sql Implementation of Comparison:
SELECT a.response, a.count_before, b.count_after
from (Select response, count(*) as count_before from input where time<timevalue groupby response) a
join (Select response, count(*) as count_after from input where time>timevalue groupby response) b
on a.response=b.response
