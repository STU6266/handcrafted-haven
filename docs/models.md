# Handcrafted Haven - Data Models

This document defines the database schemas and data structures for the Handcrafted Haven application.

## User Model
- `id`: String (MongoDB ObjectId)
- `email`: String (unique, required)
- `password`: String (hashed, required)
- `name`: String (required)
- `role`: String (enum: 'user', 'seller', default: 'user')
- `bio`: String (optional, for sellers)
- `story`: String (optional, for sellers)
- `createdAt`: Date
- `updatedAt`: Date

## Product Model
- `id`: String (MongoDB ObjectId)
- `sellerId`: String (reference to User.id, required)
- `name`: String (required)
- `description`: String (required)
- `price`: Number (required, min: 0)
- `category`: String (required, enum: 'jewelry', 'clothing', 'home-decor', 'art', 'other')
- `images`: Array of Strings (URLs, max 5)
- `inStock`: Boolean (default: true)
- `createdAt`: Date
- `updatedAt`: Date

## Review Model
- `id`: String (MongoDB ObjectId)
- `productId`: String (reference to Product.id, required)
- `userId`: String (reference to User.id, required)
- `rating`: Number (required, 1-5)
- `comment`: String (optional, max 500 chars)
- `createdAt`: Date
- `updatedAt`: Date

## Relationships
- User (seller) has many Products
- Product belongs to User (seller)
- Product has many Reviews
- Review belongs to Product and User
- User has many Reviews