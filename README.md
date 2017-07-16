# Recommendation-system-with-users-influence

An improved recommendation system demo with Yelp datasets. 

In this approach, we try to visualize the data, search communities and define users' influence to provide 
personal recommendations for users. Through mining and visualizing detected communities and users'
influence, we try to provide personal recommendation for users. A friendly user-interfase and iteractive 
visualization GUI is also be designed. You can check "method.pdf" for details. 

There are mainly two parts, and the detail information are as follow:

HAC community detection (contians the community detection algorithm):

This is the HAC program to find the communities in a graph. Given the 'pair.txt' file, which
contains pairs of users review the same restaurant. The algorithm can find the communities 
cooresponding to some stoping cretirias. There are many parameters to be choosen to find the 
best results. Here is a tried on with jac threshold 0.003 and stop loop 10000. Just simply use 
command line $python HAC.py . The final cluster will be written as a dict, and output final_community.json.
It takes some time to finish.

Recommender system and UI design (contains the recommender system and user interface GUI):

The user interface part is written in Python based on PyQt4 platform. And another necessay package 
for this application is yaml for parsing json files. You can install it by typing 'pip install pyyaml'. After 
installing these two libraries, you can use 'python ./src/yelp_ui_pyqt4.py' to run the GUI. Then in the application
window you can choose a user id to search for user specified restaurant recommendations,where the allowalbe
user ID is in the txt file 'user_id'. You can also use the restaurant name, stars and categories to 
filter the output results. The visualization results of the community and word cloud are also shown in the 
GUI. 

Community detection visualization:

![image](https://github.com/Aeroone/Recommendation-system-with-users-influence/blob/master/graphs/community.png)
![image](https://github.com/Aeroone/Recommendation-system-with-users-influence/blob/master/graphs/13916lay1.png)

GUI:

![image](https://github.com/Aeroone/Recommendation-system-with-users-influence/blob/master/graphs/GUI.png)

