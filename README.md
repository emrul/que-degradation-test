# Que Degradation Test

A simple test designed to test Que's performance under highly degraded conditions.

```
$ bundle install
$ createdb que-degradation-test
$ bundle exec sequel -m migrations/ postgres://localhost/que-degradation-test

# start a producer
$ DATABASE_URL=postgres://localhost/que-degradation-test bundle exec bin/producer

# start a worker
$ DATABASE_URL=postgres://localhost/que-degradation-test bundle exec bin/worker
```