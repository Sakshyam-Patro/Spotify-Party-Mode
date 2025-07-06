# Spotify Part Mode - Setup Guide

Getting Started

Prerequisites

Node.js 16+
Spotify Premium account (for playback features)
Spotify Developer App (Create here)
Installation

# Clone the repository
git clone https://github.com/Sakshyam-Patro/Spotify-Party-Mode.git
cd Spotify-Party-Mode

# Install dependencies
npm install

# Start the application
npm start

# Open http://127.0.0.1:3001 in your browser
Environment Setup

Spotify App Configuration

Important: Spotify has new redirect URI requirements (April 2025). Follow these steps:

In your Spotify Developer Dashboard:

Use http://127.0.0.1:3001/auth/spotify/callback (not localhost)
For production/demos, use HTTPS URLs only
Create .env file:

SPOTIFY_CLIENT_ID=your_spotify_client_id
SPOTIFY_CLIENT_SECRET=your_spotify_client_secret
SPOTIFY_REDIRECT_URI=http://127.0.0.1:3001/auth/spotify/callback
PORT=3001
Multi-Device Testing & Demos

For sharing with others or testing across devices:

# Install ngrok for secure public access
npm install -g ngrok

# In a separate terminal, create secure tunnel
ngrok http 3001

# Copy the HTTPS URL (e.g., https://abc123.ngrok.app)
# Update both:
# 1. Your .env file:
SPOTIFY_REDIRECT_URI=https://your-ngrok-url.ngrok.app/auth/spotify/callback

# 2. Your Spotify app settings in the developer dashboard
Spotify Requirements:

Use 127.0.0.1 instead of localhost for local development
Use HTTPS for production/sharing (ngrok provides this)
Exact URI match between .env and Spotify dashboard
