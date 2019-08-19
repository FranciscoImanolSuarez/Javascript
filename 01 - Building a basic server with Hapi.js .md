# Building a basic server with Hapi.js

![img](https://miro.medium.com/max/700/1*3xVhmgkXGjNfJmi3WUd_eQ.png)

Before starting to launch lines of code, I think it is better to know what [Hapi](https://hapijs.com/) is, this wonderful Frameworks is one of the most used in the ecosystem of NodeJS. It was created at Walmart by Eran Hammer, who also created the OAuth, Hammer specification. As a leader of the Mobile team at Walmart, he encountered a problem: high website traffic on days close to Black Friday.

That’s why, together with their team, they decided to create Hapi, as an express middleware, since this did not offer them a solution to the problems they faced. After trying different combinations of solutions, they decide to create the entire framework from scratch based on “Better configuration than code”.

Hapi is designed with large modularized applications in mind. It contemplates the separation of the configuration of the business logic and uses its own way of doing things. This framework is used to create web applications, API REST, API in GRaphQL, HTTP proxies and integrator of multiple Backends, among other things.

The server is the basic and main unit of web applications, so I’ll show you how to set up your own web server in minutes with these frameworks.

We will create and work in an index.js file in which we will execute all the code of this application. To create a server with Hapi, simply require the module and then run the server function:

```javascript
const Hapi = require(""hapi"")

const server = Hapi.server({
  port: 3000,
  host: 'localhost'
})
```

Then it is necessary to define the interaction points by a route:

```javascript
async function init () {
    server.route({
        method: 'GET',
        path: '/',
        handler: (req, h) => {
            return h.response('Hola Mundo!').code(200)
        }
    })

    server.route({
        method: 'GET',
        path: '/redirect',
        handler: (req, h) => {
            return h.redirect('http://google.com')
        }
    })
```

The **“method”** property indicates whether the expected request is of type GET or POST, and the path is the relative URL associated with this defined route. The controller is the function that will handle the response that will be sent to the browser.

The object **“h”** is the second argument that receives the function of controller of a defined route. This contains a collection of utilities and properties related to the response information.

Most basic methods of object **“h”**:

- h.response (): “What it does is create a response object”
- h.redirect (): “In this case, it is a request.”

The Response object (created with the h.response method) allows you to define the properties of the response. Through this object, you can specify the headers, document type and response code returned to the client, using the methods: .header (), .type () and .code ()

Also, what we can do is try and control in order to control the errors, and start a console.log that shows a message that the server is working.

```javascript
    //CONTROLAMOS EL ERROR 
    try {
        await server.start()
    } catch(error){
        console.error(error)
        proccess.exit(1)
    }


    console.log(`Servidor lanzado en: ${server.info.uri} `)
}
init()
```

Once we finish with all this, we will execute in a terminal command node.js the same will show us a message in the console that says **“Server launched in localhost: 3000”**, if we navigate to that route we should be able to see the message “Hi! world!” , and if we enter the localhost:3000/redirect route, it will take us to [**www.google.com**](http://www.google.com/)**.**

**If the article you liked or you found interesting, please help me with 👏 🤓 You can follow me on Twitter or find me on GitHub by visiting my website.**

