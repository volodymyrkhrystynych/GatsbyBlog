---
title: My AWS Journey
date: "2020-07-01"
description: Notes and links about aws
---

https://dev.to/gtanyware/lambda-and-dynamodb-the-first-steps-228


https://dashbird.io/blog/what-are-aws-lambda-triggers/


I was going through a tutorial that instructed me to create a canary lambda function, I followed it but came across a bug about the role and found the solution here:

https://stackoverflow.com/questions/36419442/the-role-defined-for-the-function-cannot-be-assumed-by-lambda

A canary function is only useful if it can notify you and in order to do that I needed to create an alert for it on AWS Cloudwatch


