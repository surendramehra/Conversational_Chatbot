# Building-a-Conversational-Chatbot-using-Rasa-Framework-deploy-on-Slack
Build a conversational Chatbot for good Restaurant discovery experience using Rasa framework &amp; Zomato API call &amp; deployed on Slack

conda info --envs
conda create -n rasa python=3.7
conda activate rasa
pip install rasa-x --extra-index-url https://pypi.rasa.com/simple
 
pip install rasa==1.9.5
pip install rasa-sdk==1.9.0
pip install ujson==1.35
pip install tensorflow==2.1.0

--Download spacy model and link it

pip install rasa[spacy]==1.9.5
python -m spacy download en_core_web_md
python -m spacy link en_core_web_md en

 

### After all setups, let's train chatbot:

$ rasa train nlu

$ rasa shell  (for testing purpose)

$ rasa train core  (It uses output of NLU)

$ rasa run action --after up the action server! run $ rasa shell --on another cmd

$ rasa interactive --that can improve training data

### If you getting error to execute the bot on terminal after using rasa train nlu/core then try: 
$ rasa train -vv -dump-stories --force 
