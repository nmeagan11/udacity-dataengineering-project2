# Project: Data Modeling with Cassandra

## Introduction

A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of CSV files on user activity on the app.

The purpose of this project is to create an Apache Cassandra database with tables designed to answer questions on song play data. To accomplish this, I will insert data in to Apache Cassandra tables by creating a streamlined CSV file.

## ETL Pipeline

The notebook <code>Project_1B.ipynb</code> explains in more detail the full ETL pipeline. In summary, we iterate through each CSV file in the <code>event_data</code> directory and use Python to read each file in and write to a singular CSV file named <code>event_datafile_new.csv</code>.

## Queries

The notebook <code>Project_1B.ipynb</code> explains in more detail the queries develped. In summary, there are three tables created from the streamlined CSV file:

| Table Name  | Columns (Types) | Primary Key(s) |
| ----------- | --------------- | -------------- |
| songInfo    | sessionId (int)<br>itemInSession (int)<br>artist (text)<br>song (text)<br>length (float) | sessionId<br>itemInSession |
| userInfo    | sessionId (int)<br>userId (int)<br>itemInSession (int)<br>artist (text)<br>song (text)<br>firstName (text)<br>lastName (text) | userId<br>sessionId<br>itemInSession |
| songLookup  | song (text)<br>userId (int)<br>firstName (text)<br>lastName (text) | song<br>userId |

## Instructions

Run through the Jupyter Notebook <code>Project_1B.ipynb</code>.
