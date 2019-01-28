# Conceptual Framework

## Objectives

We define the basic objectives of our intelligent tutoring system as follows:
- the system should be able to teach a learner regarding a subject in a dialog based format
- the system should be able to provide the learner enough aids to the learer to deepen the understanding of the subject
- the system should be able to assist the learner in revising subject for maximum retention


In order to understand the conceptual framework for building such a tutoring system, we will begin by basing our system on a simplified model of an classroom instructor. We will assume that this particular instructor instructs following a pre-defined format and takes questions at the end of the class. We also assume that this particular instructor does not possess any art of story telling to captivate the students. This particular assumption helps us to base our model such that the lectures consists only of pure information and not any trivial buffer to keep students engaged. We call this system, the unimaginative instructor. We will also assume that the system is teaching is only one student.

## The blueprint of an unimaginative instructor

In order to teach a student a particular course, the unimaginative instructor prepares a curriculum or customizes a widely used one. A curriculum dictates the relative ordering of the course topics for better understanding. The instructor divides the course into sections according to the curriculum distributed them over a number of lectures.

Breaking down a standard lecture by the unimaginative instructor
    - States the topic
    - Provides background and importance of the topic
    - Shows applications of the topics/history of the topic
    - Explain basic concepts and how it fits together with the rest of the course topics  
    - Provides examples of applications of these concepts in the real world.
    - Moves to step 1 for the next topic

The Unimaginative Instructor does the job of conveying of ideas necessary for learning the course pretty well. However, the course comprehension of the student for the course is low as the student may find the lecture dull and hard to pay attention to.

We can improve students comprehension by introduing interactivity to the instructor. 

## Conversational Tutor

In order to add interactivity, we will convert the lectures from the unimaginative instructor into text format. The lectures would be classified into the following:

- Information: A formal presentation of ideas pertaining to the topic which requires 
- Interaction: 
    - Conversation: A short informal and often personalised discussion regarding the topic. If a Conversation is used as the form of Interaction, then the last Conversation is a question or a statement that requires input from the learner. In Conversation, the learner could interact with the user using predefined replies or an input text area.
    - Widget: An interactive teaching aid. Widgets consist of multiple choice questions, reordering, fill in the blanks, match the following, an interactive chessboard, an explorable etc. 

Interaction helps in retaining the student's attention and forces the student to attempt to utilise information acquired from the course to submit inputs to the question or statement posed in the interaction. 

Each topic is broken down in sets of Interaction and/or Information. Such set of Interaction and/or Information is named Learning Atom for convience. 

The main ideas of the topic are communicated using Information, while the Interaction with the learner is done with the help of Conversation and Widgets.  

Exhibit 1 shows a Learning Atom with only Conversation
Exhibit 2 shows a Learning Atom with Information and Interaction using Converstaion
Exhibit 3 shows a Learning Atom with Interaction using Widget

The goal of each Learning Atom is to increase learner's understanding about the subject. In order to do that Learning Atom is associated with a learning objective mapped based on Revised Bloom’s Taxonomy. 

## Revised Bloom’s Taxonomy 
A group of cognitive psychologists, curriculum theorists and instructional researchers, and testing and assessment specialists published in 2001 a revision of Bloom’s Taxonomy with the title A Taxonomy for Teaching, Learning, and Assessment. 

A statement of a learning objective contains a verb (an action) and an object (usually a noun).

    - The verb generally refers to [actions associated with] the intended cognitive process.
    - The object generally describes the knowledge students are expected to acquire or construct. (Anderson and Krathwohl, 2001, pp. 4–5)

The cognitive process dimension represents a continuum of increasing cognitive complexity—from remember to create. Anderson and Krathwohl identify 19 specific cognitive processes that further clarify the bounds of the six categories (Table 1).
[Table 1]
http://www.celt.iastate.edu/teaching/effective-teaching-practices/revised-blooms-taxonomy/
The knowledge dimension represents a range from concrete (factual) to abstract (metacognitive) (Table 2). Representation of the knowledge dimension as a number of discrete steps can be a bit misleading. For example, all procedural knowledge may not be more abstract than all conceptual knowledge. And metacognitive knowledge is a special case. In this model, “metacognitive knowledge is knowledge of [one’s own] cognition and about oneself in relation to various subject matters . . . ” (Anderson and Krathwohl, 2001, p. 44).
[Table 2]

A better understanding of the picture can be seen in the figure 1.

## Learning Atom Objective 
Objective of each learning atom is mapped to a cognitive process dimension and the subsequent verb.

Exhibit 1 shows a Learning Atom with the objective to 
Exhibit 2
Exhibit 3 

In order to forumulate such integration into Interaction so that the learning objective is achieved, there are two guiding principles.

- Prior and Posterior Self Learning
- Known to Known Mapping

## Principle of Prior and Posterior Self Learning

The central idea of conversational learning is to implement Prior and Posterior Learning (PPL). In Prior and Posterior Learning, the agent questions the learner about his prior understanding about a certain topic. After the learner replies his own ideas about the topic, the agent replies with the accepted answer about the topic. The user can self-evaluate his own understanding and the accepted answer provided by the agent. This lets user to understand the gaps present in his understanding and accepted understanding in case he is way off. In case the user's understanding of the topic is correct, this reinforces confidence in the learner. 

It can be noted that the agent doesn't offer *correct* answer rather an accepted answer. It is to reinforce the idea that the agent can be wrong and so can be the accepted answer. It also presents a possibility that the learner can stumble upon an understanding that is counter-intuitive to the accepted understanding resulting in innovation.  

An example of such Learning is shown is the Exhibit 4 about a user who is incorrect in his assumption and an example of such learning where the user is correct is shown in Exhibit 5.

## Principle of Known to Known Mapping

The other principle used to achieve the learning objective of the Learning Atom is named Principle of Known to Known Mapping. It is based on the idea that every topic is built on the foundations of ideas resulting from one or more sets of information. The role of instructor is often to demonstrate how the topic can be built from its reference information. This results in the learner passively absorbly ideas that may or may not map into the learner's knowledge database. 

In Known-to-Known Mapping, the instructor provides all neccessary information as ingredients to derive the required information to the learner and the learner use the avaiable ingredients to infer the topic's central gist. This is an example of active learning by the learner. This principle is hard to replicate in live instructor led classroom due to constraint of time and in a recorded lecture due to lack of interactive input. 

A conversational learning agent implements the principle of known-to-known mapping in the following way:
- The agent poses questions about the related concept that it believes the learner is aware of
- The agent asks the learner to relate the concepts and hints towards the topic objective 
- The learner may or may not be able to derive the topic but a sincere effort results in deeper understanding.

Such a system ensures that the new knowledge being added to the system maps to something that the user already is aware and enriches the knowledge data base.

[Exhibit 6 explaining the principle of Known to Known Mapping]
[Exhitibit 7 explining the principle of Unknown to Known Mapping]

A dialog script is generated based upon the above two principles to achieve the learning objectives of each Learning Atoms. The script is used by the conversational agent to instruct the learner. 

This is basic conceptual framework of the Intelligent Tutoring System. 

Although, the tutoring system is ready to instruct the learner, it needs to be extended for better understanding of the learner. 

# Extending the Tutoring System


## Summarizing Prompt
At the end of each topic, the learner is provided an opportunity to explain their understanding about the recently learned topic. This helps the learners in formulating their understanding in concrete statements in their own language. This user created summary is also added to the Automatically Generated Notebook at the end of the course.  

If a learner is facing difficulty into explaining the concepts and information, then it is taken into account by feedback system. How well the dialog script for the topic is able to achieve its learning objective is tracked with Explainability Metric.

## Explainability and Dialog Script as a Software

The explain-ability of the course refers to the number of students who took the course and number of students who found the agent was lacking in providing the information to understand the topic.

        E = 1 - total number of students who found the agent lacking   / total number of students to took the course  * 100

This is provided by the students in the feedback system which also asks the students to pinpoint which topic or subject was more difficult to understand to. Feedbacks without reasoning is not taken into consideration for calculating explainability.

High explainability for a topic demands the course script to modified and improved. This posits the course script to be akin to a software which improves itself on every release and is versioned accordingly. The topic which has low explainability can be modified to divide up into smaller parts to facilitate better understanding and the usage of creativity to provide understanding.

In order to deepen the understanding, the course often carries a project component, which the learner needs to complete before the learner can complete the course. 

## Project

The project component of the tutoring system is a tools agnostic dialog script that underlies a real world problem statement and uses the newly acquired course concepts to solve them. With the help of project,  the agent guides the learner in understanding the application of the topic in the problems. Example of such a project is building a convolutional Neural Network from scratch and using to for image classification for a realworld dataset.


## Learner notes and questions

At any point during the topic or during revision, the learner has the ability to add notes and questions. 

There system allows different forms of notes:

- Topic Notes: Notes written during the course
- Revision Notes: Notes written at the time of revision
- Questions: Questions that arises in the mind of learner
- Equation Notes: Notes written against a equation

Additionally, all the terms and definition introduced in the topic are compiled together for easier access of the learner. The learner can also coin new terms and its defintion for better retention. 

## User Questions

The Tutoring system also includes a community forum where the learner can post their questions. After certain interval, the questions are compiled and added to the dialog scripts in their next improved version. The tutoring system also helps the learner to document their answer for their questions. 

## Auto Generated Notebooks

At the successful completion of course, the learner can generate a personalised course notebook in the portable document format(PDF). This document contains lecture notes, learner's notes, responses, terms and questions.  

This is provided to free the subject of any compulsion during the course to scribble down on paper and provide utmost attention to the topic being taught. The notebook also acts a course journal which can be revisited even after a period of time and will be easier to understand due to its personalised nature.

A sample notebook can be seen here.

## Revision and Auto Generation of Flash Cards

The responsbility of the tutoring system also includes that the learner retains the topics learnt during course. After completion of any topic, the learner can revise the topic by going through the conversation with the agent regarding the topic. Also after the topic is completed, predefined flashcards relevant to the topic are added to the revision deck. Apart from that, flash cards are generated from the learner's notes, completed questions and terms. 

The flash cards generated from user notes is done by first dividing the lines into string of separate sentences and then eliminating the stop words from the sentence. Stop words are the words in the language which appear frequently but doesn't provide additional meaning to the sentence. 

[Exhibit of Flashcards generated from User Notes]

## Retention

The responsibility of the agent also includes ensuring that the subject retains the course in the long term. In order to do that, there are two kinds of facilities for revision provided:

- Spontaneous Revision of Topic

After the completion of any topic, the spontaneous revision option is enabled and the subject can go back and browse through the conversations with the agent. Completing the flash cards associated with the topics is considered as the completion of revision.

- Scheduled Revision of Topic

Once the course is completed,  in order to ensure that the effort spent during learning the course is not wasted, the conversational agent draws up a revision schedule. 

The revision schedule consists of a five term revision separated at certain intervals of days in order to implement Spaced Reptition. The revision schedule is based on mean average \textbf{retention score} for all the topics present in the course. 


## Retention Score


Retention score is calculated with the following equation:

$$R = 10e^{\frac{-t}{s}}$$

Here R = Retention Score , t = time passed since topic completion or revision completion and s = retention strength of the topic. 

Retention Strength depends on:

- Number of topic notes the user has added
- Number of revision notes the user has added
- Number of questions the user has proposed and answered
- Number of terms the user has defined
- Number of Equation Notes the user has defined.

Retention score has been created to put a quantitative figure on the subject's retention. Though there is no evidence for any correlation existing between the retention score and the actual retention, it acts as a proxy for putting a number to the decaying knowledge. 

- When the user completes the topic, the R = 10 with t = 0. As time passes the Retention score decreases while strength remains constant.

When a person completes a scheduled revision, revision is reset to 10 and strength goes up. Though spontaneous revision resets the retention score to 10, it doesn't affect the retention strength. 

The purpose of Strength is add an incentive whose effect is visible to the user. The following figure demonstrate the visible effects of revision.

[Figure of Retention Score]


## Incentives for completion and revision

The tutoring system takes into account that the learner will lack discipline to complete through the course or to revise the contents frequently. In order to deal with the issue, the system incorporates incentives.

- Incentives for course completion is that the personalized notebook and flash cards are generated only after course completion.
- Incentives for revision is to keep up the retention score  
- Incentives for adding notes, terms and questions is to increase the retention strength for the retention score.


## Ending Note for Intelligent Tutoring System

The intelligent tutoring system outlined above is a basic framework for building an dialog based tutoring system. It has been designed to be extensible, customized to the needs of the topic. Such system will help anyone who wishes to learn difficult topics without a human actor.

