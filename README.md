# Audio Transcription Service - CS6620 Group 9

A cloud-based audio-to-text transcription service built with AWS serverless components.
Users upload audio (MP3/WAV/M4A), the backend runs AWS Transcribe, and the frontend provides
interactive previews, karaoke-style playback, and subtitle downloads.

## Features
- Upload audio (MP3, WAV, M4A; max 25 MB)
- Automatic transcription using **AWS Transcribe**
- Download transcripts and subtitles (JSON, SRT, VTT)
- Live/partial preview while jobs are running
- Karaoke-style word highlighting and click-to-seek
- Presigned upload/get URLs for secure file transfer

## Architecture
- **Frontend**: Static HTML/JS/CSS (AWS Amplify or S3 + CloudFront)  
- **API**: AWS API Gateway (REST)  
- **Backend**: AWS Lambda functions (presigned URL generation, Transcribe starter, results processor)  
- **Storage**: AWS S3 (separate `uploads/` and `results/` buckets)  
- **Database**: AWS DynamoDB (job metadata, status)  
- **Transcription**: AWS Transcribe (async jobs)  
- **Monitoring**: CloudWatch Logs & Metrics

## Deployment
- Frontend: connected to AWS Amplify
- Backend: deploy Lambda + API Gateway
