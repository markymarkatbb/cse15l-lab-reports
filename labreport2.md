
![c050a5fe96833af265e59262ad37c94f](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/86e5b33b-623a-4c27-8f79-21259eea173c)

![119839dad91015fb7448d8bcbb835d47](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/486ae30a-d4c8-4a80-9e5b-30653858d9e1)
![6dde07ee9252c0ed2ccf2f7841a6fcf2](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/b0223e30-e685-47d5-8f39-0780d3007851)

I implemented a simple chat server in Java that can handle HTTP requests and maintain a chat history. When building this server, I focused on the essential functionality needed to meet the requirements laid out in the lab instructions.

The server is designed to handle requests to add messages via a specific path (/add-message). 
I set up the ChatHandler class to handle requests by checking if the path equals /add-message, which was a little trickier than I initially thought because I had to consider how to extract and split the query string correctly. 
I used the split method on the query string with & as the delimiter to separate the parameters, and then again with = to get the values for the user and message parameters.

![968a6c5a905ddfbedeea42c90710e575](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/a99f8c18-e20d-41c1-b2f1-1665de940eb5)
![c930fc71e467e77943b8b121dc20a5ed](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/1b54f63c-ca1f-404a-a145-8dc9e67d2a42)
The output "jpolitz: Hello" after the first curl request was expected due to how the handleRequest method in the ChatHandler class is written to append each new message to the chatHistory string, which was initially empty. 
the server's handleRequest method in ChatHandler was called, which interpreted the query parameters and updated the chatHistory string with "jpolitz: Hello". 
The server then returned this chatHistory, which is why the terminal outputted "jpolitz: Hello".

For the second curl request, the method's consistent behavior appended "yash: How are you" to the chatHistory, which already contained "jpolitz: Hello", and this is why the output cumulatively showed both messages, precisely as the code dictates. 
this triggered the handleRequest method, which again parsed the query parameters and concatenated "yash: How are you" to the existing chatHistory. 
So, the server's response included both the original and new messages, producing the extended chat history in the terminal.


![7ba876c3cea0a47fe9f6c42dfaf06ada](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/b7fb5bce-6959-4dbd-83b2-37a31d3f4bdb)
![d35cefd0e4e0cd2ca56bf466dfcfc728](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/d16f8973-ccb0-440b-be4f-6f9fe85da6d9)


In the last two weeks it was definitely interesting that I learned about SSH keys; it's like having a special pass into another world—definitely a peek into what high-level programmers must be dealing with. And working with others in my lab was helpful in learning
how operating with other individuals might work especially getting into each others local host servers.
It might not be something I'll use every day, but it was fun to see how I could get into another server so seamlessly. Makes me wonder the kind of access a hacker or high level programmer must have into systems.






