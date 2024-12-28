# intelligent-call-center


#!/bin/bash
chmod +x new-code.sh
# Step 1: Create a new React app
echo "Creating a new React app..."
npx create-react-app call-with-chat
cd call-with-chat

# Step 2: Install required dependencies
echo "Installing dependencies..."
npm install @mui/material @emotion/react @emotion/styled @azure/communication-calling @azure/communication-chat @azure/communication-ui-library @azure/communication-identity

# Step 3: Create CallWithChatComponent.js
echo "Creating CallWithChatComponent.js..."
cat <<EOF > src/CallWithChatComponent.js
import React, { useEffect, useRef, useState } from 'react';
import { Box, Button, Typography, Paper, CircularProgress } from '@mui/material';
import { CommunicationIdentityClient } from '@azure/communication-identity';
import { CallClient, VideoStreamRenderer } 
