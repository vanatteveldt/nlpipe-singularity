# nlpipe-singularity
Singularity Image for NLPipe

1. Build the image:

```{sh}
sudo singularity build nlpipe.img Singularity
```

2. Run the alpino service:

```{sh}
singularity instance.start nlpipe.img nlpipe
```

3. Run the worker:

```{sh}
singularity run --app worker instance://nlpipe /tmp/nlpipedata alpinocoref
```

4. To test, run (in a separate shell) the client:

```{sh}
singularity run --app client instance://nlpipe /tmp/nlpipedata alpinocoref process_inline "dit is een test"
```

which should print an XML file after about 10 seconds. 

(Note: these are my very first steps into singularity-land, so all feedback is appreciated!)
