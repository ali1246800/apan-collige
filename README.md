#!/bin/bash

# Define variables
SERVER_USER="your_user"
SERVER_IP="your.server.ip.address"
REMOTE_DIR="/path/to/your/project"
BRANCH="main"

echo "Deploying to $SERVER_IP..."

ssh "$SERVER_USER@$SERVER_IP" << EOF
  cd $REMOTE_DIR
  git pull origin $BRANCH
  echo "✅ Code pulled successfully!"
EOF



c
