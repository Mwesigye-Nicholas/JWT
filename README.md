# JWT Authentication Mini Project 🎉  

![JWT Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c8/JSON_Web_Token_Logo.svg/1200px-JSON_Web_Token_Logo.svg.png)  

## Table of Contents  
- [Overview](#overview)  
- [Features](#features)  
- [How It Works](#how-it-works)  
- [Usage](#usage)  
- [License](#license)  

## Overview 📚  
This project is designed to deepen my understanding of **JSON Web Tokens (JWT)**. It implements JWT for user authentication, providing a secure and efficient method for managing user sessions.  

## Features ✅  
- **Token Expiry**: Each generated token has a limited lifespan of **60 seconds** to enhance security.  
- **Refresh Token**: A refresh token is issued to allow the generation of new access tokens after the initial token expires.  
- **Revocation Mechanism**: A function to disable tokens is implemented, ensuring that users do not have permanent access through the refresh token.  

## How It Works 🔧  
1. **User Login**: Users authenticate and receive an access token and a refresh token.  
2. **Access Token**: The access token is valid for **60 seconds** and needs to be included in the headers of requests.  
3. **Token Refresh**: After the access token expires, the user can use the refresh token to obtain a new access token.  
4. **Token Revocation**: Users can have their refresh tokens disabled, which prevents further access and enhances security.  

### Token Lifecycle Diagram 🗺️  
```plaintext  
User Login → Access Token (Expires in 60s)   
        ↓       
Refresh Token → New Access Token (repeats)