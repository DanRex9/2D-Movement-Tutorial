# 2D-Movement-Tutorial
A tutorial on how to add simple 2d left & right movement in unity

# Prerequisites
Before approaching this tutorial, you will need a current version of Unity and a code editor (such as Microsoft Visual Studio Community) installed and ready to use.

This tutorial was created with Unity 2022.3 LTS and Microsoft Visual Studio Community 2022 versions. It should work with earlier or later versions. But you should check the release notes for other versions as the Editor controls or Scripting API functions may have changed.

You will have to know how to create 2d objects in unity and how to create folders and organise your files in the projects folder.

# Objectives
In this tutorial, we will be leatning how to write a simple script for 2d movement.

# Getting Started
The first thing we are going to do is in the hierarchy create a 2d square sprite and name it `Platform` make it as large as you wish and nothing else as this will only our floor, the again in the hierarchy crate another 2d square and this time call it `Player` once you have done this head over to the inspector and add these componenets `Box Collider 2D` and `Rigidbody 2D` in the rigidbody change `Collision Detection` to Continuous and the `Interpolate` to Interpolate, this is so we get smooth movement all the time.
Now create an scripts folder and create a `C#` name it `Movement` and open it. your script should look like this.

<img width="846" alt="Screenshot 2025-01-05 at 01 52 08" src="https://github.com/user-attachments/assets/eb3fa2e4-e4d8-4d38-9d8d-7cd41b47cdf6" />


# Coding Movement
Now in our scripts lets create a `Public float` for `speed` and for `Move`
In our Update` function we are going to set the our Move float to our left and right input keys with this code. This is so when we are in unity at the press of one of these keys it will move in that direction.

<img width="846" alt="Screenshot 2025-01-05 at 01 56 04" src="https://github.com/user-attachments/assets/cdb5269f-c759-4017-9901-b79962b8b81b" />
<img width="846" alt="Screenshot 2025-01-05 at 01 55 54" src="https://github.com/user-attachments/assets/f90892a4-5829-4cf9-8ccb-635f84938695" />

Now we have to make a reference to our Rigidbody by writting a `private Rigidbody2D rb` at the top and in the `Start` function we can write this line of code to asign it to our player in Unity. 
[`Start`](https://docs.unity3d.com/2017.1/Documentation/ScriptReference/MonoBehaviour.Start.html)

<img width="818" alt="Screenshot 2025-01-05 at 02 02 55" src="https://github.com/user-attachments/assets/d805d748-ede9-418a-a12e-6a75414e55b9" />

Now we can set the velocity of our Rigidbody to a new Vetor2 in which for the x axis we can multiply our `Move float` by are `speed float` to create left and right movement
[`Vector2`](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Vector2.html) and this is all the scripting needed, tour script should now look like this.

<img width="637" alt="Screenshot 2025-01-05 at 02 15 37" src="https://github.com/user-attachments/assets/98a2da9e-6795-4901-91e8-6eeea459cafc" />

# Finishing 

Now back in unity select your player and drag our `Movement` script we just wrote and add it as a component into our player and here you can set the speed to what ever you would like, for the sake of testing it you can set it to 7, now click play in Unity and now you should have simple Left & Right 2D Movement. 

And you are finished.

I got the reference for this tutorial from https://www.youtube.com/watch?v=Azh5QuGLDcU
