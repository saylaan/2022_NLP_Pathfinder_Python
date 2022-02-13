# Getting Started

The travel order resolver was an application created containing three components: The voice, the Natural Language Processing (NLP) and the pathfinder. The voice component records the voice of a user to a file. The NLP component transcribed this file and saved it to a text file. Later the text is analyzed for a valid train travel request and the departure and destination extracted. The pathfinder component took these two locations and used a graph structure to determine the fastest route between them. Later an application was created to use this functionality.
Keywords: Natural Language Processing, Pathfinder, Artificial Intelligence, train

For having more information about the project and the methodology, please see the document "Report.pdf" in the root of the project`

## The components

You can see all the three component necessary for the project in the folder `/docs/jupyter-components`
There you will have :

- Audio recorder 
This component will record an audio sample, and save it to an audio file.

- NLP component
This component takes an audio file and writes its content to a text file

- Transcript component
This component takes a text file and extracts a travel request destination and departure

- Pathfinder component
This component takes a departure and destination, and calculates the fastest path between the nearest train stations to these locations.

## Launch interface

The infrastructure is made in Python with Flask framework

You have two possibility to use the app, with a container docker or a basic installation on your environment.

### Container docker

1. First, you need to go to the infrastructure directory `cd /app`

2. Run the script `./launch_server.sh`

3. Open a browser and go to the page `http://localhost:5000/`

### Basic installation

1. First, you need to go to the infrastructure directory `cd /app`

2. Then, you need to install all dependencies `pip install -r requirements.txt`

3. Install all this module :
`pip install langdetect`
`pip install icecream`
`pip install spacy`
`python -m spacy download fr_core_news_md`

4. If you have any missing module during the installtion. Just run the command `pip install name_module`

5. After the project installation is complete, you can launch the app by going in `cd /app/back` and run the command `python app.py`

## Troubleshooting

Make sure that your current working directory for the project is at the root of the repo
