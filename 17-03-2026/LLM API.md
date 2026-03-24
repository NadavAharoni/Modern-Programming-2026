# Summary of Feature Development – LLM Integration on a Shopping Site

Rut Froulich / 17-03-2026

In this project, I presented a new feature that I developed to integrate artificial intelligence capabilities into a shopping site. The feature allows the display of a book summary in real time, immediately after the user clicks the 'Add to Cart' button. At the moment of clicking, the book title is automatically sent to the server, which passes it to Groq's AI model. The model returns a summary in Hebrew, which is displayed to the user as a popup, significantly improving the browsing experience.

## How Does the Feature Work

The system is built from a simple and efficient information flow:

1.  The user clicks 'Add to Cart'.
2.  The client side (Angular) sends a request to the server with the book title.
3.  The server (C#) builds a prompt in Hebrew and sends it to Groq.
4.  Groq returns a summary in Hebrew in JSON format.
5.  The summary is immediately displayed as a popup on the site.

## What Did I Actually Develop?

On the client side (Angular):

1.  Calling the server API.
2.  Receiving the summary from the server.
3.  Displaying a popup window to the user.

On the server side (C#):

1.  Building a quality prompt in Hebrew.
2.  Sending a POST request to Groq.
3.  Retrieving the summary from JSON.
4.  Returning clean text to Angular.

Everything is done in real time with just one click.

## Why Did I Choose Groq?

After testing several AI services, Groq was the only one that worked smoothly:

## Insights from Development

- Integrating AI into an existing website is simpler than it seems.
- It is important to choose a model that returns stable JSON.
- The quality of the prompt directly affects the quality of the result.
- It is better to call AI from the server rather than from the browser.
- The feature can be expanded to include descriptions of additional products.