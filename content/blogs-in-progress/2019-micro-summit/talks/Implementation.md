Data science life cycle

start
V
business understanding
W
Data acquisition and understanding
W
Deployment
W
Modeling

#Problems
proper logging
sub 300ms response time for data processing while customer is
switching pages

serverless app size allows for fast response but has its own
problems

#Solutions

make small modifications
test integration
ready-made frameworks (chalice)
Shadow environemnts
AWS kambdas
level-based logging
domain-based architecture
separate cross-cutting concerns

##Result
a large set of seperate microservices
Ruby microservice talks to customers
ruby microservice talks to python chalise micro ml
data lake of sql, nosql, s3 interfaced using presto
