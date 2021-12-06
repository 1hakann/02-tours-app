React project 2: Tours
This project deploy here Tours App: https://1hakann.github.io/02-tours-app/

To clone the project
git clone https://github.com/1hakann/02-tours-app.git In the project directory, you can run: npm run start Node must be installed to run the project.

Description
This app is one of the objects that can be filled arbitrarily, giving a json from listing objects. In doing so, some features are gained. Remove it for a content. A little one also makes the list. The Loading screen for the view at the time the data was captured is displayed. It is also run and used separately to create long texts. Design is an example. However, it will be in directing the writing of the css.

In this second step, the information and examples learned in Birthday Reminder were reinforced, even some extra features were included in the app using javascript. These features can also be added to the Birhday Reminder App if desired. So go back and make version 2 yourself and share it with me.

Let's see what we've done now:
First of all, useState, data file, css and List component were imported in App js.

In this second step, the information and examples learned in Birthday Reminder were reinforced, even some extra features were included in the app using javascript. These features can also be added to the Birhday Reminder App if desired. So go back and make version 2 yourself and share it with me.

Let's see what we've done now:

First, we created the Tours, Loading components. We imported css. We imported useState and useEffect. Then we created the api and defined the url. Remember in our first app our data was a json file. This time an api. Therefore, we get the url with a variable.

The second thing we need to do in our app is to define our variable sets. As you know, we use useStates here. Taking our components to be run conditionally with useStates as default false and using them when true. Let's add the loading i like this. Then, let's add our Tours component to meet our data [] as an empty array.

Now let's try something new in this app and pull the data from the api. So let's fetch.
For this, we have defined an arrow function with async feature. first setLoading true at the beginning
It will enable our other page to be displayed by giving

Then we added the try catch structure because there are data operations, we gave catch setLoading false and we pushed the error to the console. We come to try and here we perform our main operation. Let's define the respnse variable. Take url as fetch method parameter and add await. Now you have a response variable like nurtopu. This time, let's add our tours variable and convert our response variable to json() and add await again. Let's get this last variable with setTours right after setLoading gives false.

The third step will take us to the main point. We can activate our UseEffect. It will help us sort our data by streamlining it as an array. Let's create the arrow as a function. Let's call our fetchTours() method, in which we have assigned our function above. Then we add ,[]. This will insert each given content into the array.

Let's call the fourth name if loading and return a separate page. Here we completed it by adding Loading components under main. Then we simply defined our Loading component. We just imported React. We have defined an arrow function.

Let's return a design inside. I just added a simple loading text. You can do much more. Now let's define the App's own return. Here we will use our Tours component so that we can list our contents. For this, let's define an attribute called tours in our component and send it in return tours u {}.

Now let's go back to our Tours component. Each component you add will have a standard setup. Of course, it grows and goes according to these features. In its most basic form, React import starts with installing it as a class or function and exporting it with the import of other components that it will use in it. It becomes ready to use with the parent tags of the return method.

We took tours u {} as a parameter. In accordance with our design, we divided our tours into parts within a div with the map method. We created an arrow function in the map. We sent tour as a parameter. We added a Tour component in Return that will list each content. We added the key attribute and defined it as tour.id. With a modern use of {...tour} after it, we have access to all of our objects.

After that, let's prepare our Tour component. We will be processing our data and we want to add some javascript features so we added useState. If we are parameters, we add the keys of each of our tours. Like id, image, info, name.

Now, we can call the data we want in the necessary places of our list card, which we designed with css before, such as ${price}, {name}. Let's test it. taa.

Now let's get our first dynamic feature. Let's add readMore as a variable. Let's meet with Usestate. Let's encode readMore in return {} with ternary if. Here you can make use of the substring() method. You can specify the range with the two numerical values ​​you give. Then let's define onClick for our button. Let's call the setReadMore method with !readMore inside

Our application is almost ready to be deployed. Let's add a few more distinctive and mind-opening features. Let our tours be removed from the list. There are many ways to do this. A good option is to parent all of them in one class and pass them on to the children. So back to the App

We can add it after our variables. I defined an arrow function called removeTour. We give the id as the parameter. Since the new list created after deletion is always a new list, we can create a cons variable and name it newTour. This time we will use the filter method with tours. Let's create an arrow function inside. Let's give tour as the parameter and say tour.id !== id. Then let's call the setTours method with the newTour parameter.

Now it's time to transfer this to tours. For this, let's define the attribute with the same name in our component and this time send our method in {}. Let's go to our Tours object and welcome our method at {}. So let's take it. Now we will transfer the method to the tour components from here. For this, let's go to the Tour by doing the same to the Tour component. Now let's design a button here and use our method by giving it onClick. We give the id as the parameter.

So what happens when all the content is gone? Something not in our first app! Let's put the Refresh button-. For that, let's go back to our App.

But if it is not ready yet, you can work with css while our ready data can be viewed to beautify your view. You can then continue where you left off. I will continue.

If tours.length is 0, let's define the condition and add a button in it, then let's define onClick. Let's call fetchTours(). Let's test it. Well done!

Deployment
Now it's time to deploy.

For this, let's add a homepage to package.json. Let's add git remote set-url as origin. Then let's add the predeploy and deploy commands to the scripts. Now let's do npm install gh-pages --save-dev. Now let's perform the build and then deploy operations. That is all.

See you in the next app. Goodbye! Stay with the code.
