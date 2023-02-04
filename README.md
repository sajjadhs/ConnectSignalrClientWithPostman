
# Connect to a SignalrClient with Postman

For connecting to a SignalR hub by postman need to follow this:

Make a succesful connection to your server using hub endpoint

By very first message should send protocol message

    {"protocol":"json","version":1}

***Note:** Copy above line completely with the special charachter to specify end of message. Otherwise your request won't be processed by your server.


Now you can call needed method using this message structure:

    {
        "type": 1,
        "target": "MethodName",
        "Arguments": ["IfAny"]
    }

There is that special char at the end of this message as well :)

If you follow correctly should get this response:

    { "type" : 6 }

I hope could help 🤞
