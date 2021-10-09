# Creating Instagram API using Golang

![badge](https://img.shields.io/badge/Appointy-Technical%20Task-%23099DFD)

![image](https://user-images.githubusercontent.com/60420648/136669881-8f875faa-2767-4171-ac80-2ac1026bdb48.png)

### Requirements

* Golang SDK. See the [Golang SDK](https://go.dev/) installation instructions.
* An IDE that supports Golang. You can install *Android Studio, IntelliJ IDEA, or Visual Studio Code* and install the Golang plugins to enable language support and tools for refactoring, running and debugging your backend. I personally prefer Visual Code.

## Commands to run

* To start a local project using Golang

go mod init <project name>

* To add packages to our project

go get <package name>



## Steps to run

Run the following commands to run the project

```
go build main.go
go run main.go
```


### Disclaimer
I have not used a .env file for the MongoDB Uri now for ease of evaluation. I can do the same while working on real life projects.

### The API consists of following endpoints: <br/>
1. /users GET Request: Get all users
2. /users PUT Request: Create a user
3. /users/id GET Request: Get user by id
4. /posts GET Request: Get all posts
5. /posts PUT Request: Create a post
6. /posts/id GET Request: Get post by id

<br/>
<br/>

#### The model of the API looks like:
```
type User struct {
	ID       primitive.ObjectID `json:"_id,omitempty" bson:"_id,omitempty"`
	Name     string             `json:"name,omitempty"`
	Email    string             `json:"email,omitempty"`
	Password string             `json:"password,omitempty"`
}

type Post struct {
	ID        primitive.ObjectID `json:"_id,omitempty" bson:"_id,omitempty"`
	Caption   string             `json:"caption,omitempty"`
	ImageUrl  string             `json:"imageUrl,omitempty"`
	Timestamp time.Time          `json:"timestamp,omitempty"`
	
}
```
### Sample Tests
Create a new user             |  Get all posts
:-------------------------:|:-------------------------:
![image](https://user-images.githubusercontent.com/60420648/136670000-2d54f6b2-6f98-407f-94c0-6dd82290c7ad.png)|  ![image](https://user-images.githubusercontent.com/60420648/136670036-f629b0eb-8753-409b-8edb-282778032e94.png)	
	
