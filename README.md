# Text Genius · Backend

Spring Boot backend for **Text Genius**, a GenAI writing helper. It wraps the OpenAI Chat Completions API with ready-made prompts for three jobs: summarize a paragraph, write a short explainer on a topic, and translate text into another language.

**Portfolio:** [utkarash-thakur.vercel.app](https://utkarash-thakur.vercel.app)

## Highlights

- Three endpoints, each with its own prompt template that tells the model the role, the task, the output format and the answer language.
- Answers in any language the user asks for, such as Hindi or Punjabi.
- Model, temperature, token limit and timeout are set in `application.properties`.
- CORS config for the frontend and a global exception handler.

## Tech stack

Java 17 · Spring Boot · Spring Web · OpenAI Chat Completions API · Maven

## API

All endpoints take `{"prompt": "...", "language": "..."}`.

| Method | Path | What it does |
| --- | --- | --- |
| POST | `/summary` | Summarize the paragraph as a one-line takeaway plus key points |
| POST | `/generation` | Write a 60 to 100 word explainer on the topic |
| POST | `/translation` | Translate the text into the given language |

## Run locally

1. Put your own OpenAI API key in `Mesh/src/main/resources/application.properties` (do not commit it).
2. From `Mesh/`, run `./mvnw spring-boot:run`.
