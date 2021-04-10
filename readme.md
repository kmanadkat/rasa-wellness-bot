# Wellness Check Rasa ChatBot

This is rasa based chatbot. User is asked several health related questions and at the end the logs are shared back to the user. This project demonstrates how easy it is to create NLP based chatbots with rasa opensource sdk. It mainly consists of a Form and Custom Actions. A beginner friendly scope was kept so that any one looking for getting started, could refer this.

## Setup and Installation
It is recommended to use Python 3.6 or Python 3.7 with rasa framework. Below are the steps to run this project.

1. Clone master branch of this repository & open root directory in terminal.
2. Create virtual env with python: `python3.7 -m venv ./venv` and activate it by `source ./venv/bin/activate`
3. Install rasa `pip install rasa`, with this you can now run rasa commands described below.

### Generating Trained Model
Make sure python virtual env is active in terminal. Change directory to `backend` & run rasa train like below. After training is done, you will find `models` directory at `backend/models` this is the result of rasa NLU training & rasa Core training.

```shell
cd backend
rasa train
```

### Running Actions Server
After training is done, you need to run server to serve custom actions related computation. Open another terminal instance, activate virtual env and open `backend` directory.

```shell
rasa run actions
```

### Running Rasa Chatbot in Shell
Below command loads the trained model, opens communication to custom actions running server & provides REPL to interact with chatbot.

```shell
rasa shell
```

## Chatbot Screenshots

**rasa train**

<img width="1594" alt="01 rasa-train-success" src="./images/01 rasa-train-success.png">


**rasa run actions**

<img width="1016" alt="02 rasa-run-actions-success" src="./images/02 rasa-run-actions-success.png">


**rasa shell - happy flow 1 - affirmed for exercise**

<img width="1525" alt="03 rasa-shell-happy-flow" src="./images/03 rasa-shell-happy-flow.png">


**rasa shell - happy flow 2 - denied for exercise**

<img width="1528" alt="04 rasa-shell-happy-flow-no-exercise" src="./images/04 rasa-shell-happy-flow-no-exercise.png">


**rasa shell - sad flow 1 - going out of scope & coming back**

<img width="1523" alt="05 rasa-shell-sad-path-1" src="./images/05 rasa-shell-sad-path-1.png">


**rasa shell - sad flow 2 - going out of scope & denied to proceed**

<img width="1525" alt="06 rasa-shell-sad-path-2" src="./images/06 rasa-shell-sad-path-2.png">
