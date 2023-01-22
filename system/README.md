This folder contains the developed user study system, including three
frontend applications and one backend server.

To run the system, you need to compile the frontend applications, then
run the backend server.

## Frontend

To compile the frontend applications, you need to install `nodejs` and
`npm` first. Then run the following commands:

Text domain

```
cd frontend/listwise-ranking-text && npm i && npm run build
cd frontend/listwise-ranking-image && npm i && npm run build
cd frontend/listwise-ranking-mesh && npm i && npm run build
```

## Backend

As described in the paper, the backend includes multiple services. Except for the core backend collection service, it also includes a Bayesian optimizer and three domain services.

### Domain services
Domain services include 1) text summarizer, 2) image color enhancer, and 3) mesh simplifier.

#### Text summarization service

Text summarization service is an independent service that runs a dedicated
python server. To run the service:

```
pip install -r requirements.txt
cd backend/services/text-sum
python main.py
```

TODO: add text summarizer.

#### Photo color enhancement service

Photo color enhancement service is integrated into the core backend service, and reproduces this [paper](https://koyama.xyz/project/SelPh/index.html). See also https://github.com/yuki-koyama/enhancer.

#### Mesh simplification service

Mesh simplification service is also integrated into the core backend service and reproduces this [paper](https://doi.org/10.1145/3543758.3543761). See also https://changkun.de/s/infloop.

### Optimizer service

The optimizer service is implemented in Python, and the core service invokes the Python script to run the optimizer.
The core service supplies arguments to the optimizer.
The optimizer will fetch the data based on the core service
naming convention from the file system, then compute the next suggestion and returns the result to the core service.

TODO: add the optimizer service.

## Core service

To run the core server, one must run the server with underlying environment support, especially for python, e.g. be able to find BoTorch. It is recommended to run the server in a virtual environment, such as `conda` or `virtualenv`.

```
cd backend && make run
```

## Interface and Access Frontend

The developed frontend interface is only useable if the requested URL contains these query parameters: `user_id`, `session_id`, and `study_id`. For example, the following URL is valid:

```
/prefprior/text/listwise/ranking/?user_id=changkun&session_id=this_is_a_session&study_id=this_is_a_study
```

In this case, the `user_id` is `changkun`, the `session_id` is `this_is_a_session`, and the `study_id` is `this_is_a_study`.

