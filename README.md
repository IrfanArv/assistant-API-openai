# About

This is a simple code example on how to work with [assistant API by OpenAI](https://platform.openai.com/docs/assistants/overview).

## Set up

1. Add your OpenAI API key
   Copy the `env.txt` to `.env`  
   Add your openAI API key

1. Get assistant id
   You can create a new assistant via GUI (platform.openai.com) or programmaticaly and get the id  
   Add the ID to the `.env` file as well.

## How to run

Install packages

```
npm install
```

Run server

```
node server.js
```

**Test at postman**

- Open postman or other HTTP client
- Hit `http://localhost:3000/thread` with GET method
- Copy the threadId
- Hit `http://localhost:3000/message` with POST method
  Attach this as `Body > raw > json`

```
{
    "message": "your message",
    "threadId": "your_thread_id"
}
```

You can play with your assistant, by sending multiple messages to the same thread id.
