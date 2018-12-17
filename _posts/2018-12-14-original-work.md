---
layout: post
title: "Original Work"
date: 2018-12-14
excerpt: "2018-2019 ISM Original Work"
project: true
tag:
- project
- python
- NLP
comments: false
---

# Original Work Proposal

<iframe src="https://drive.google.com/file/d/1GfgNARdvitkgi6y13Cjfz6Tbm1gE5_Ji/preview" width="710" height="600"></iframe>

# Project

* Most of my research for this project can be seen under the Research tab in both the primary and secondary assessments. Below is the first test of my purely machine learning-based program. It has some difficulties at this point, but I'm eager to make changes and will post updates on it in the future. 

<iframe src="https://drive.google.com/file/d/1rYBu6IEHEwmVLddYvrpiJzy9hZtXqSD_/preview" width="710" height="500"></iframe>

* Most of my code revolved around simply accessing data

<code>c.execute("CREATE TABLE IF NOT EXISTS parent_post(id int PRIMARY KEY, comment_id TEXT UNIQUE, parent_id TEXT UNIQUE, parent TEXT, comment TEXT, subreddit TEXT, score INT)")
 with open("D:/redditData/RC_{}".format(file_time), buffering=1000) as f:
        for row in f:
            row = json.loads(row)
            comid = row['id']
            comtext = format_data(row['body'])
            score = row['score']
            parid = row['parent_id']
            parid = parid.split("_")[1]
            subreddit = row['subreddit']
            partext = find_parent(parid)
            #inserting rows into database
            if (useful(comtext, parid)):
                entry = (comid, parid, partext, comtext, subreddit, score)
                c.execute('insert or replace into parent_post values(?,?,?,?,?,?)', entry)
c.execute('insert or replace into parent_post values(?,?,?,?,?,?)', entry)
</code>

* or manipulating it to, for example, create even lengths in the data arrays.

<code>inputs = np.array(pad_sequences(inputs, maxlen=sent_length))</code>

* The simplest, yet most emphasized part, was the implementation of the Long Short-Term Memory model and corresponding layers within it.

<code>
model = Sequential()
model.add(Embedding(len(dictionary), 10, input_length=19))
model.add(LSTM(128, input_shape=(input_array[0]), activation='relu', return_sequences=True))
model.add(Dropout(0.3))
model.add(LSTM(128, activation='relu', input_shape=(input_array[0]), return_sequences=True))
model.add(Dropout(0.3))
model.add(Dense(128, activation='relu'))
model.add(Dropout(0.3))
model.add(Dense(len(dictionary), activation='softmax'))
model.compile(loss='categorical_crossentropy', optimizer=Adam(lr=1e-3, decay=1e-5), metrics=['accuracy']) 
model.fit(np.array(input_array), np.array(target), batch_size=100, epochs=20, validation_split=0.1)
</code>

* Finally, a list of some of the changes I plan on making in future versions. This analysis provides all of the ideas I will change in the next iterations of this project, and will come partially as a result of implementing more of the Amazon developer skills for NLU and TTS processes.

<iframe src="https://drive.google.com/file/d/1pwy7tuX-pdxHRPWz7d3VPDNOeWNuEecL/preview" width="710" height="600"></iframe>

# Set-Up and Completion Summary

<iframe src="https://drive.google.com/file/d/1j8_xncMvYRYldLuBLcxEGOkwx8QM7Ovq/preview" width="710" height="600"></iframe>

# Original Work Assessment


