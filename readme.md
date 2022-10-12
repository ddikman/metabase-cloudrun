# metabase on cloudrun

This was an experiment to see if I would be able to host a metabase instance on cloud run to make it available only when used.

The result however, was that it isn't possible. Metabase takes too long to start up and is not suitable for paralell runs. You have to have one single persistance instance that serves the same connections over time.


## deploy

```shell
gcloud builds submit --region=eu
```