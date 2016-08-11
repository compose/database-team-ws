# Database Team Work Sample

Welcome to the Compose Database Team work sample! This sample should take you between 2-8 hours, depending on your familiarity with the subject matter. There is no time-limit and no deadline - we encourage you to take all the time you need in order to create a submission that you are proud of.

We work hard to preserve the anonymity of those submitting work samples to us. This is considered a 'blind' exercise that will judge you on your technical merit alone. Please do not place identifying information within the work sample! As a result of the fair, objective, and anonymized nature of the samples, we are unable to give you any assistance outside of this document.

Please note that we do not provide feedback in the event of an unsuccessful submission. We do this to preserve the mysterious nature of our grading criteria.

## Context

At Compose, we provide databases-as-a-service. To date, we host several open-source management systems, including:

* PostgreSQL
* MongoDB
* RethinkDB

In addition, some neat tools including:

* etcd
* RabbitMQ
* Elasticsearch
* Redis

The database team that you are working to join is responsible for making sure each database meets the customers' expectations and is a good steward while running on top of the Compose platform. We do exploratory research on running new database. We also do research and analysis on databases currently running on Compose to see how we can improve either the customer experience or our own experience with the database.

Thus, this work sample will test your ability to orchestrate a point-in-time-restore (PITR) feature with a command line tool. Because we use Python for most of our database orchestration, this tool will be built in Python.

## Getting started

Ideally, the tool should take the base database files and the WAL archive, and apply the WAL archive onto the base database files to achieve a point in time recovery.

All of the bits are in the pitr file. We've removed some logic and created some errors as part of the test. First, get the pitr completing a point in time recovery, then feel free to improve the tool for point in time recovery.

# Things to consider

* this script will probably be run by other scripts, this should exit 0 when
  successful and exit 1 when unsuccessful.
* this script will fail, when it does fail, the more precise the error
  the better.
