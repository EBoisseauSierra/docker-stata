# Usage

You can build the image locally on your own. First, you must have Stata installer in `.tar.gz` format (Stata for Linux) and save it in this directory `(./base-stata/)`

```bash
# build image locally
docker build -t base-stata .

# run image
docker run -d -it --name=base-stata base-stata:latest
docker exec -it base-stata bash

# stop container
docker stop base-stata

# remove container if no longer needed
docker rm base-stata
```

Note that prior to running Stata, you need to populate the `stata.lic` file inside `/usr/local/stata/` directory. Otherwise, you will get the following error message when you prompt Stata batch mode:

```
Cannot find license file
stata.lic
```
