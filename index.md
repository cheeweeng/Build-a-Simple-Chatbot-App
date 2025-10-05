This exercise will use [Flowise hosted on Hugging Face](https://cheeweeng.github.io/Setup-Flowise-on-Hugging-Face/) to build a [LLM-powered English-to-Japanese translator app](https://github.com/user-attachments/assets/b17fd520-a4c2-4872-9b1f-da4a14b920d0).  
Login to Hugging Face 🤗 and click on the workspace created.  
At Chatflow dashboard, click “Add New” , a new “Untitled Chatflow” canvas is created.  

The + icon on the top left is to add node.  
Click on + icon and search for LLM Chain. Drage it onto the canvas.  
 
<img width="500" height="400" alt="Image" src="https://github.com/user-attachments/assets/ce099d8a-8e1e-47f6-be7d-879830e6cf89" />

Next, search for the ChatOpenAI node and drag onto the canvas.    
On the ChatOpenAI node, connect the credential and select the LLM model.  
In the ChatOpenAI node, click on Additional Parameters and fill in the various fields as below. 

<div style="display: flex; gap: 10px; justify-content: center;">
  <img width="500" height="450" alt="Image 1" src="https://github.com/user-attachments/assets/c905d9ae-03b1-448f-86c5-1f8c1b760c49" />
  <img width="400" height="480" alt="Image 2" src="https://github.com/user-attachments/assets/27c904a4-e8d2-4ca5-b57c-cca84b557528" />
</div>

In the add credential, name the credential and paste your OpenAI API key.  
<img width="400" height="200" alt="Image" src="https://github.com/user-attachments/assets/771bf4c0-2e83-45ae-94a1-966bf872a676" />  

Next, search for Chat Prompt Template node and drag it onto the canvas.  
#### System Message:  
You are a helpful, friendly and bilingual assistant. You will be asked for assistance in {input language}. You are to provide two responses. One paragraph in {output language} and the other paragraph in {input language}  
#### Human message:  
{text}  

Click on the Format Prompt Values.  Input the input and output_language and text by clicking on the pen icon (edit).  
The input language is English and choose your preferred output language - Japanese, French, Spanish or Chinese.  
For text, enter  {{question}}.
<div style="display: flex; gap: 10px; justify-content: center;">
<img width="500" height="400" alt="Image" src="https://github.com/user-attachments/assets/bb798050-b403-4720-bb19-fe30eb7cd1a5" />
<img width="380" height="180" alt="Image" src="https://github.com/user-attachments/assets/c0fcaeaf-d8c1-490c-a1b5-9cda7d2de440" />
</div>  

## Connecting the nodes  
Connect the output of ChatOpenAI and Chat Prompt Template into the Language Model and Prompt of LLM Chain node respectively.  
Save the chatflow and give it an approriate name. The chatbot is ready to start chatting.
<img width="800" height="600" alt="Image" src="https://github.com/user-attachments/assets/e2dc5dcb-cde0-48c4-a8e5-3855221d0626" />    

Here's a glimspe of the chat messages.  
Click here for [video demo of the chatbot](https://github.com/user-attachments/assets/b17fd520-a4c2-4872-9b1f-da4a14b920d0)    
 
<p><img width="320" height="550" alt="Image" src="https://github.com/user-attachments/assets/68221471-f947-4cd3-854a-c27f5d0cb0e7" /></p>
  
Back to [Projects Portfolio](https://cheeweeng.github.io/)
