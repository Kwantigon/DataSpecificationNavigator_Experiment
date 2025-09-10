# DataSpecificationNavigator_Experiment

This repository contains the necessary files for the DataSpecificationNavigator experiment.

You are given 3 questions in natural language. Your task is to write a SPARQL query for each of the given question.

You can use a local [Apache Jena Fuseki](https://jena.apache.org/documentation/fuseki2/) instance to test your SPARQL queries against the provided dataset.
The instructions for setting it up are [below](#setting-up-a-fuseki-instance).

## Requirements

- Have [docker](https://www.docker.com/) installed.

## Setting up a Fuseki instance

Go to the fuseki directory.

```bash
cd fuseki
```

1. **Start Fuseki**

	 - On **Linux**:
		 ```bash
		 ./run_fuseki.sh
		 ```
	 - On **Windows**:
		 ```cmd
		 run_fuseki.bat
		 ```

2. **Upload the dataset**
	 
	 - On **Linux**:
		 ```bash
		 ./upload_data.sh
		 ```
	 - On **Windows**:
		 ```cmd
		 upload_data.bat
		 ```

3. **Access the SPARQL endpoint**

	 Open your browser at: [http://localhost:3030/#/dataset/tourist-destination/query](http://localhost:3030/#/dataset/tourist-destination/query)

	 When prompted for login credentials, use:

	 - **Username:** `admin`
	 - **Password:** `pass`

When you want to stop the Fuseki container and remove temporary database files, run the `remove_fuseki` script.

- On **Linux**:
```bash
./remove_fuseki.sh
```
- On **Windows**:
```cmd
remove_fuseki.bat
```

## Working on the questions

With the Fuseki instance set up, you can now work on the questions in the experiment.

1. Open Tasks_GroupA.md
2. Work on one question at a time, in order.
3. Before starting each question, start a stopwatch.
4. When you finish writing your query, stop the stopwatch and record the time taken.
5. Write your query in the space provided.
6. Write your recorded time in the space provided.

If you do not have a stopwatch, you can use an [online stopwatch](https://www.timeanddate.com/stopwatch/).

For each question, write a corresponding SPARQL query.

When you are done, save the `Tasks_GroupA.md` file and submit it.

## Submitting the result

Please send your save `Tasks_GroupA.md` file to me on Mattermost. You can either send a DM or send it as a reply to my thread.

Don't forget to stop the running Fuseki container and remove its database files.

- On **Linux**:
```bash
./remove_fuseki.sh
```
- On **Windows**:
```cmd
remove_fuseki.bat
```
