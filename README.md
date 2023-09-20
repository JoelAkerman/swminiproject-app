# SuperChat - Real-time Chat App with Firebase and React

SuperChat is a real-time chat application built using React and Firebase. It allows users to sign in with their Google account and engage in real-time chat conversations. This README file provides an overview of the code structure and functionality of the application.

# Overview

SuperChat is a real-time chat application that leverages Firebase for authentication and Firestore for real-time database functionality. It consists of the following key components:

App: The main application component that handles user authentication and routing to different sections of the app.
SignIn: Component responsible for allowing users to sign in with their Google account.
SignOut: Component for signing out the currently authenticated user.
ChatRoom: The core chat room component that displays messages in real-time and allows users to send new messages.
ChatMessage: Component for displaying individual chat messages.

# Code Explanation

Firebase Configuration
The Firebase configuration is set up at the beginning of the code using firebase.initializeApp. It initializes Firebase with the necessary credentials for authentication and database access. Replace "YOUR_API_KEY", "YOUR_AUTH_DOMAIN", and other placeholders with your actual Firebase project credentials.

# Components

## App

The App component is the entry point of the application. It manages user authentication and renders different sections of the app based on whether a user is signed in or not.

If a user is signed in, it renders the ChatRoom component.
If no user is signed in, it renders the SignIn component.
SignIn

The SignIn component provides a button that allows users to sign in using their Google account via Firebase authentication.

## SignOut

The SignOut component displays a "Sign Out" button if a user is currently authenticated. Clicking the button logs the user out.

## ChatRoom

The ChatRoom component is where users can engage in real-time chat. It displays messages in real-time, allows users to send new messages, and automatically scrolls to the latest message.

It uses the useCollectionData hook to fetch and display messages from the Firestore database.
Users can input new messages and send them using the input form.
Messages are automatically scrolled to the latest one using the dummy ref.

## ChatMessage

The ChatMessage component is responsible for rendering individual chat messages. It differentiates between messages sent by the current user and received messages, applying different styles accordingly.

This README provides an overview of the SuperChat application and its code structure. For more details on specific code components and functionality, refer to the inline comments in the code itself.
