## Group Members

- Sai Krishna Chilvery:
    - Designing, implementing, and managing the web servers or web services that receive user requests.
    - Coordinating with other components, especially with the app-tier, by routing user requests appropriately, typically through the requests SQS queue.
    - Constantly monitor the responses SQS queue and direct the responses to the corresponding users.
    - Design the Web-tier AMI to be plug and play. This means, the entire application should be able to be deployed with just the web-tier AMI.
- Akash Reddy Maligireddy:
    - Work alongside web-tier development to implement auto-scaling.
    - Monitoring the depth of the requests SQS queue at regular intervals (every 10 seconds) to make scaling decisions.
    - Implementing the linear scaling logic, where the app-tier scales up or down in direct proportion to the queue depth, with specific constraints like capping at 20 instances and ensure that at least 1 app-tier instance is always available.
- Sadaf Shaik:
    - Build on the top of the provided Image recognition AMI. Consume the requests SQS queue to fetch tasks for processing and subsequently pushing results or responses to the responses SQS queue.
    - Integrating with storage solutions, like the Images S3 Bucket and Labels S3 Bucket. The consumed images are directed to the images bucket and the predicted labels to the labels bucket.
    - Serve App-tier as a one-shot AMI to ensure loose coupling with the web-tier instance and auto-scaling mechanisms.

## AWS Credentials

Console sign-in URL: https://660567238494.signin.aws.amazon.com/console

Username: cse546-admin

Password: P@ssw0rd!

PEM KEY: `connection_secret.pem`

-----BEGIN RSA PRIVATE KEY-----
MIIEpAIBAAKCAQEAli3OgqFIHzZvsq3vYcYtII+Os3qg/2lzOXe9CuSuFtBsRa8m
94nQqTXPab7/GDMbjyAzo8KMahxxfdZIR4P8r3QnNv783G3GqzukycKtNAJuCXM6
A5TuzhokGX4BJSoIowVJIucsqCd+tWN6G31J5zE/1gKte6DajlGf52pcuddxCCW/
slz2AxBDg3YaQdrwkg1HsK0gawbGPW9Wpr7A88qdTaxyXQGMAgw+y+9J9r5lJqyb
mYCBxAr5u1qY0vdR+1RmtXuknogEBnuldpQV1YEk10iKtuLfoEnBu42hdXehXzhq
BlUqQNAhb+3idxVtYPwfXiLp1lrCvTpGQ5ZNwQIDAQABAoIBAB4Jg2h1Qaucg7LF
Pz/bF2OP0wbq3BC50qYH4POw0XEWttEpOy3/jpCJhrar0PHSJwz1b96tJtCCZ+C3
XzWOnJerL7y8O28LNdVB1K/WFDZ21fNl7JCS1UC70cSXgzsfsSKKCBrHChOH8rvs
7ZtZ79Ih85amanRzs8MLaGQszecNc5cuqxtcAek7PKDcoqjfdJbLSJHG+wjQgI2C
6jlFvIppsomKuSxUpavbkhFKZR4tifBQONFN5Ue67Ql4EDFIYQjYmMdS/4ya5ZXi
NMSD5os29muPle2qSYl868bJGzwGKErzb2xZ2u54d/pbFMc9tCv/00iP5HOid0Bf
7zP+ZtECgYEA+FusIvk1zunXAw0qWLlnVDf+X2sQ0mXfRYU+PNFUFlws4yIi3zwh
RgGuishp0fQIeihzxiVPXo1TNLxZIJLJ6ExzGmqolCRupIqShzTabHROXfZGpqj4
0RIqXKrHxzlmRl32zhaceBi5j+qKtMHU90At+Agdo67puy8JtXaBis8CgYEAmszF
0BY2IIMh24dhK5dAzdYJm4mBfmFsYM6faW88dj+v6SKbaUZClnSVrYNRKMkViOp+
VraKiOUABAgL08gEbrys7Py1ZpK8wfp4LsPcSYselwUjTBYI2hAREveF1SJ+y7X0
JUak8g11+8ma0SsWNblLyPWO5u9LUbbUAFuygm8CgYEAlN3GMXR1p2ANLFwQ3PvN
DvM9Ow6fF65OhYpXgvbqUzjPAxpsEqklPKQ3biKxI1MGXcqvkr68c218yWh4eAjk
k6R3fgceoyWvWFtjdz3cCxQwASxkrvMrqY4c7EzF0Qn73wPlsyRkh6wyVix9Fdn1
gHrs0vZyZbGrkjKgvC+beIsCgYB41rboLB6OnK7WZsTUuVquE5ImZ129oSFwJHtO
W7YP/ME+NXSp5l3egx3AeAzn0KjN23dKC27zVAgCHaHV7YKASyqWSOL2Mj/FENe2
cdBJXJ9BdpJKN70rNHWPn8dKTIY8UUpHuvDRvu5F4efHtmG9CGt/cSjfXxclr5mo
uewMYwKBgQCwYjzLDZbPEIgAHVl1UJuFdwg5UVE8a0WBzXGQc5zk14w5o2ka57Ns
yS5XtbPSfe7QAlb7FdOy6kCZV65UnKy3hHN2u6ged7tvWbZEtm1mSLjSYb4z67TR
L86WrqCjim9H1QcU8yJNoKgccn/QNIUzfvuAWj62tTUFemH2rBvkSA==
-----END RSA PRIVATE KEY-----

## Web Tier URL

> http://ec2-54-86-239-253.compute-1.amazonaws.com:8080/

## Resources

### SQS Queue Names
 - cse546-1-requests
 - cse546-1-responses

### S3 Bucket Names
 - cse546-1-images
 - cse546-1-labels

### EIP

> 54.86.239.253


