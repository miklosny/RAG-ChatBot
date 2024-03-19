## This Repo is for creating RAG system using LangChain and Streamlit

### Python Environment

#### 1. Install Packages

```b
pip install -r requirements.txt
```

#### 2. Set Api Key

- Create a new openai api key, link: https://platform.openai.com/api-keys.

<img src="Images/create_api_key.png" alt="create_api_key" style="zoom:80%;" />

- Copy it into .env file

​	Set OPENAI_API_KEY="Your API KEY"

#### 3. Run Simple Version On Colab
- Input your openai api key in the ChatOpenAI() 
```
llm = ChatOpenAI(model_name="gpt-3.5-turbo", openai_api_key="")
```

- You can change embedding model by searching on HuggingFace.
```
HuggingFaceEmbeddings(model_name="sentence-transformers/xxxxxxx")
```

- Ask question and get answer on Colab.


![](Images/simple colab version.png)	
#### 4. Run Streamlit On Colab
- Input your openai api key in the ChatOpenAI() .
```
llm = ChatOpenAI(
    model_name="gpt-3.5-turbo",
    temperature=0.1,
    openai_api_key=""
)
```

- You can change embedding model by searching on HuggingFace.
```
embedding = HuggingFaceEmbeddings(
    model_name="sentence-transformers/all-MiniLM-L6-v2",
    model_kwargs={"device": "cpu"}
)
```

- You can get an url, but you don't need to click on it, stop this cell.

![npx url](Images/npx url.png)

- Run the next cell, get the tunnel password.

![get curl password](Images/get curl password.png)

- Run the above cell again, click the last url link.

![password UI](Images/password UI.png)

- Enter the tunnel password, which you got in the previous step. Then you can see the Streamlit WebUI.

<img src="Images/streamlit ui.png" alt="streamlit ui"  />


#### 5. Run Streamlit On Local Computer

```
streamlit run app.py
```
