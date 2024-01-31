## ChatServer Code:
![code](img/code.png)

## First /add-message:
![chat1](img/chat1.png)

Methods called: 
```
handleRequest()
```

Arguments:
```
url =  localhost:4000/add-message?s=hi&user=jason
```
Fields:
```
parameters = ["s=hi","user=jason"]
s = ["s","hi"]
user = ["user","jason"]
conversation = "jason: hi\n"
```
How Fields Change:
```
parameters, s and user all change because the query being inputted changes.
conversation changes because it is appended by the variable s[1] and user[1].
```
## Second /add-message:
![chat2](img/chat2.png)

Methods called: 
```
handleRequest()
```

Arguments:
```
url =  localhost:4000/add-message?s=hello&user=brandon
```
Fields:
```
parameters = ["s=hello","user=brandon"]
s = ["s","he;;p"]
user = ["user","brandon"]
conversation = "jason: hi\nbrandon: hello\n"
```
How Fields Change:
```
parameters, s and user all change because the query being inputted changes.
conversation changes because it is appended by the variable s[1] and user[1].
```

## Absolute Path to Private Key
![privatekey](img/privatekey.png)

Absolute Path: 
```
/c/Users/brand/.ssh/id_ed25519.pub
```
## Absolute Path to Public Key
![publickey](img/publickey.png)

Absolute Path: 
```
/home/linux/ieng6/oce/22/bjonathan/.ssh/authorized_keys
```
## Login with no Password
![nopasslogin](img/nopasslogin.png)

## New Things I Learnt in Week 2 & 3
I learnt how new commands such as ssh which allows for me to connect to the university's computer remotely to execute commands from my own laptop. I also learnt how a basic server with query works because of how the program reads a URL.
