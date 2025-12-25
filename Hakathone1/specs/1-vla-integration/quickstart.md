# Quickstart Guide: Vision-Language-Action (VLA) Integration

## Prerequisites

- ROS 2 Humble Hawksbill installed
- Python 3.8+ with pip
- OpenAI API key (or local alternatives for Whisper/LLM)
- Robot with ROS 2 compatibility (or Gazebo simulation)

## Setup

### 1. Clone and Initialize
```bash
git clone <repository-url>
cd <repository-name>
git checkout 1-vla-integration
```

### 2. Install Dependencies
```bash
pip install openai
pip install torch torchvision torchaudio
pip install ros2
# Additional ROS 2 packages as needed
```

### 3. Environment Configuration
```bash
# Set up environment variables
export OPENAI_API_KEY="your-api-key"
export WHISPER_MODEL="base"  # or tiny, small, medium, large
```

## Running the VLA System

### 1. Start the Core Services
```bash
# Terminal 1: Launch ROS 2 system
ros2 launch vla_system system.launch.py

# Terminal 2: Start the VLA services
python -m vla_core.main
```

### 2. Test Voice Command Processing
```bash
# Send a test voice command
curl -X POST http://localhost:8000/api/voice/process \
  -H "Content-Type: application/json" \
  -d '{
    "audio_data": "<base64-encoded-audio>",
    "user_id": "test-user"
  }'
```

### 3. Generate Cognitive Plan
```bash
# Create a cognitive plan from a natural language command
curl -X POST http://localhost:8000/api/planning/generate \
  -H "Content-Type: application/json" \
  -d '{
    "command": "Move forward 2 meters and pick up the red object",
    "user_id": "test-user"
  }'
```

## Module Structure

The VLA system is organized into three main modules as specified:

### 1. Voice-to-Action Pipeline (`module-4/01-voice-to-action.md`)
- Speech recognition with Whisper
- Voice command processing
- Conversion to robot commands

### 2. Cognitive Planning (`module-4/02-cognitive-planning.md`)
- LLM-based task decomposition
- Natural language goal processing
- ROS 2 action sequencing

### 3. Capstone Autonomous Humanoid (`module-4/03-capstone-autonomous-humanoid.md`)
- End-to-end system integration
- Full VLA pipeline demonstration
- Voice → Plan → Navigate → Perceive → Manipulate

## Running the Full Pipeline

1. Ensure all services are running
2. Use the voice processing API to submit commands
3. Monitor plan execution status
4. Observe robot actions in simulation or on physical hardware

## Troubleshooting

- If speech recognition fails, check audio input quality and API key
- If LLM planning is inaccurate, review prompt engineering
- If robot actions fail, verify ROS 2 communication and robot status