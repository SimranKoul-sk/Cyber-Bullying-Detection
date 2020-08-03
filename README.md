# Cyber-Bullying-Detection

INTRODUCTION
With the increasing use of social media like Facebook, cyberbullying behavior has received
more and more attention. Bullying is defined as intentional aggression carried out repeatedly by
one individual or a group of individuals towards a person who is unable to easily defend him or
herself Cyberbullying includes sending, posting, or sharing negative, harmful, false, or mean
content about someone else. It can include sharing personal or private information about
someone else causing embarrassment or humiliation. Some cyberbullying crosses the line into
unlawful or criminal behavior. The abundance of public discussion spaces on the Internet has in
many ways changed how we communicate with others. These discussions can often be
productive, but the anonymity that comes with hiding behind a username has allowed users to
post insulting or inappropriate comments. These posts can often create a hostile or
uncomfortable environment for other users, one that may even discourage them from visiting the
site. In 2017, about 50% of young social media users reported being bullied online in various
forms. Popular social media platforms like Twitter and Facebook are not immune, as racist and
sexist attacks may even have caused potential buyers of Twitter to balk.
Cyberbullying may cause many serious and negative impacts on a person’s life and even lead
to teen suicide. The detection of cyberbullying is often formulated as a classification problem.
Techniques typically used for document classification, topic detection, and sentiment analysis
can be used to detect electronic bullying using characteristics of messages, senders, and the
recipients. To reduce and stop cyberbullying, one effective solution is to automatically detect
bullying content based on appropriate machine learning and natural language processing
techniques.
This project focuses on can extract the comments from any post on Facebook and detect the
cyber bullying by doing sentiment analysis. Sentiment refers to the use of natural language
processing to systematically identify, extract, quantify, and study affective states and
subjective information. is the interpretation and classification of emotions (positive, negative
and neutral) within text data using text analysis techniques.

Cyberbullying has grown as an important societal challenge nowadays. The Cyberbullying
affects both in terms of psychological and emotional means of a person. So, there is a need to
devise a method to detect and prevent cyberbullying in social networks. Most of the existing
cyberbullying methods involves only text detection and few methods are available for analyzing
the visual detection.
Booming of social networking leads to the extensive spread of cybercrimes such as
cyberbullying, which is a quite severe problem for teenagers. Traditional studies of cyber-crime
such as bullying stand more on a macroscopic view. Conducted by scientists and psychologists,
those studies focus on the statistics of cyber-bullying and how to prevent them in a psychological
way. As big social network service providers all APIs for academic research, instead of doing
statistical study on limited sampled data, researchers are able to access to much larger corpus by
using data crawling, which further drives the development of the computational study of
cyberbullying based on machine learning and natural language processing techniques.

Sentiment analysis of short texts such as single sentences and Twitter messages is challenging
because of the limited contextual information that they normally contain. Effectively solving this
task requires strategies that combine the small text content with prior knowledge and use more than
just bag-of-words. One introductory work has been presented in one of the papers, in which several
NLP models such asBoW, Latent Semantic Analysis (LSA) and Latent Dirichlet Allocation (LDA)
have been applied to detect the signals associated with. Bullying in social
media. Their outcomes have already been verified the possibility of automatic cyberbullying
detection. Dinakar et.al used Lin-ear Discriminative Analysis to learn label specific features and
combine them with BoW features to train a classifier. The length of label-specific features is limited
to be less than the class numbers, which creates problems for the performance boost. Nahar et.al
magnified the weights corresponding to bullying words by a double. This work shares a similar
motivation with the construction of bullying features in our model that bullying features should be
enhanced. However, they did not consider the words’ semantics and the scaling operation was quite
arbitrary. In addition, Nahar et.al [15] also adopted topic models including Probabilistic Latent
Semantic Analysis (PLSA) and Latent Dirichlet Allocation (LDA) to learn
topics and performed feature selection, which is conducted over topics that feature that
comes under bullying-like topics are preserved. However, the determination of bullying-like
topics lacks a general theory basis.

5. METHODOLOGY
➢ We have created a corpus of commonly used negative phrases, words and facts, by using
Selenium library to scrape the web and extract them. For training of our model, we have
used the movie reviews dataset which is available in the NLTK corpus. This dataset has
actual review text annotated along with their associated sentiments. Now, we have to
generate the testing data. This can be done by using SocioFi tool which is a third party
application which is used to extract real-time Facebook comments in reaction to posts on
the social media platform. This data is not labeled and our model will predict the
sentiment label based on the text in the comments.
➢ First, we generate the corpus of the negative and abusive phrases or words and factual
negative phrases using import and use Selenium driver. The driver will scrape the web
and create a corpus of these words and phrases which we will further use as the
abusive word corpus.
➢ We then import the NLTK corpus from the TextBlob library, which includes the movie
reviews dataset with labeled reactions that will be used as our training dataset. After that,
we will create a Naïve Bayes classifier, which will train on the reviews text available in
the movie reviews using the abusive word corpus. This will further generate a polarity
and subjectivity score for each of these texts and a final label as abusive, negative,
factual negative, neutral, positive, etc. is predicted. Now, based on the actual label and
the predicted label, the model learns.
➢ We will similarly create a Support Vector Machine classifier that trains on the same
movie reviews dataset using cyber bullying corpus. For test data generation, we will use
Sociofy that is a third party application to scrape Facebook and retrieve comments on
posts. This will extract all comments and reactions from the Facebook along with the
user id that are posted. The models are independently tested on these extracted Facebook 
comments. The models analysis the sentiment and subjectivity of each and every
comment and set certain parameters according to the user beyond which the negative
sentiment must not be tolerated.
➢ When the comments are predicted negative by the system, the abusive words in that
comment are found and mapped to the abusive word corpus. These comments are then
categorized into labels like abusive, negative, factual negative, neutral and positive
based on the model’s prediction only after they have generated the polarity and
subjectivity scores for each of these comments.
➢ After the whole process is completed, the user ids are stored which are mapped with
the reaction user ids. If any user has posted any abusive content on the post but the
reaction posted seems to be positive, then it will not be booked for cyber bullying
because it maybe some sarcastic comment according to the admin of the post.
➢ In the end, we plot a bar graph for the percentage of comments in each category
predicted by both the models separately.

PROPOSED MODEL
In this project we have intended to build a system in which we can extract the comments
from any post on Facebook and detect the cyber bullying by doing sentiment analysis. The
system will then segregate the comments as positive, negative, abusive, neutral, facts, etc. the
main function of this model is that we have mapped the comments of the user with the
reactions given by the same user to make the model more accurate.
For example, a boy posts a photo and some of his friend posts abusive comments but along
with a ‘friendly’ react on the post then that particular comment will not be considered as
abusive or insulting because the friend has posted this comment with a good intention.
Additionally, this model is also compatible of translating the given text in any language into
English and further doing the Sentiment Analysis. By this procedure, we have visualized
the results in an interactive manner such that even a naïve user will be able to understand
the exact statistics.

CONCLUSION
We have used Sentiment analysis for detecting cyber bullying. We created a Naïve Bayes
classifier, that trains on the review text available in the movie reviews, using the abusive word
corpus, which generates a polarity and subjectivity score, for each of these texts, and a final label
as abusive, negative, factual negative, neutral, positive. This system will then segregate the
comments as positive, negative, abusive, neutral, facts thus helping us detect comments that
come under cyberbullying.

REFERENCES
[1] C. Nobata, J. Tetreault, A. Thomas, Y. Mehdad, and Y. Chang. Abusive Language Detection in Online
User Content. In WWW, 2016.,6
[2] D. Santos, C. Nogueira, and M. Gatti. Deep Convolutional Neural Network for Sentiment Analysis of
Short Texts. COLING, 2014.,13
[3] Divyashree, H. Vinutha, N. S. Deepashree. An Effective Approach for Cyberbullying Detection and
Avoidance. International Journal of Innovative Research in Computer and Communication Engineering,
2016.,14
[5] G. E. Hine, J. Onaolapo, E. De Cristofaro, N. Kourtellis, I. Leontiadis, R. Samaras, G. Stringhini, and J.
Blackburn. A Measurement Study of 4Chan’s Politically Incorrect Forum and its effort on the web. In
ICWSM, 2017.,3
[6] H. Hosseinmardi, S. A. Mattson, R. I. Rafiq, R. Han, Q. Lv, and S. Mishra. Analyzing Labelled
Cyberbullying Incidents on the Instagram Social Network. InSocInfo, 2015,1
[7] Huang, Minlie, Y. Cao, and C. Dong. Modelling Rich Contexts for Sentiment Classification with LSTM.
arXiv preprint arXiv: 1605.01478, 2016.,12
[8] I. Kayes, N. Kourtellis, D. Quercia, A. Iamnitchi, and F. Bonchi. The Social World of Content Abuser in
Community Question Answering. In WWW, 2015.,5
[9] J. M. Xu, X. Zhu, A. Bellmore. Learning from Bullying Traces in Social Media. University of WisconsinMadison, 2016.,22 [10] J. M. Xu, X. Zhu, and A. Bellmore. Fast Learning for Sentiment Analysis on
Bullying. In WISDOM, 2012.,10
[11] K. Dinakar, R. Reichart, and H. Lieberman. Modelling the Detection of Textual Cyberbullying. The
Social Mobile Web, 11, 2011.,7
[12] L. Engman. Automatic Detection of Cyberbullying on Social Media. UMEA UNIVERSITY, 2016.,15
[13] Pradheep. T, Yogeshwaran.T, J.I.Sheeba, S. Pradeep Devaneyan. AUTOMATIC MULTIMODEL
CYBERBULLYING DETECTION FROM SOCIAL NETWORKS, 2016.,17
[14] V. Nahar, S. Tankard, X. Li, and C. Pang. Sentiment Analysis for Effective Detection of Cyberbullying.
In APWeb, 2012.,9
