# Audio Transcription Service - CS6620 Group 9

A cloud-based audio-to-text transcription service built with AWS services.

## Features
- Automatic transcription using AWS Transcribe
- Download subtitles in multiple formats (SRT, VTT)
- Real-time job status tracking

## Architecture
- **Frontend**: Static HTML/JS hosted on AWS Amplify
- **Backend**: AWS Lambda (Serverless)
- **API**: AWS API Gateway
- **Storage**: AWS S3
- **Database**: AWS DynamoDB
- **Transcription**: AWS Transcribe

## Deployment
This app is automatically deployed via AWS Amplify when changes are pushed to the main branch.