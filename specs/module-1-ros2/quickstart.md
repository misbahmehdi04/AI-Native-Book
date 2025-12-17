# Quick Start Guide: Module 1: The Robotic Nervous System (ROS 2)

## Prerequisites

Before starting this module, ensure you have:

1. **Basic Python Knowledge**: Familiarity with Python syntax and concepts
2. **ROS 2 Installation**: ROS 2 Humble Hawksbill installed on your system
   - Ubuntu 22.04 LTS (recommended) or Windows 10/11
   - Python 3.8 or higher
3. **Development Environment**:
   - Text editor or IDE (VS Code recommended)
   - Terminal/command prompt access
4. **System Requirements**:
   - At least 4GB RAM
   - 2GB free disk space

## Setting Up Your Environment

### 1. Install ROS 2 Humble Hawksbill

Follow the official installation guide: [ROS 2 Humble Installation](https://docs.ros.org/en/humble/Installation.html)

For Ubuntu:
```bash
# Add the ROS 2 apt repository
sudo apt update && sudo apt install curl gnupg lsb-release
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(source /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null

# Install ROS 2 packages
sudo apt update
sudo apt install ros-humble-desktop
sudo apt install python3-colcon-common-extensions
```

For Windows, follow the Chocolatey-based installation instructions in the official documentation.

### 2. Source ROS 2 Environment

Add this to your shell startup script (~/.bashrc for bash or ~/.zshrc for zsh):
```bash
source /opt/ros/humble/setup.bash
```

Or source it manually each time:
```bash
source /opt/ros/humble/setup.bash
```

### 3. Verify Installation

```bash
ros2 --version
```

You should see the ROS 2 version number printed.

## Running Your First ROS 2 Node

### 1. Create a Workspace

```bash
mkdir -p ~/ros2_ws/src
cd ~/ros2_ws
colcon build
source install/setup.bash
```

### 2. Try a Built-in Example

```bash
# Terminal 1: Start a talker node
ros2 run demo_nodes_cpp talker

# Terminal 2: Start a listener node
ros2 run demo_nodes_py listener
```

You should see messages being passed between the nodes.

## Module Structure

This module consists of three chapters:

### Chapter 1: ROS 2 Fundamentals
- Understand the role of ROS 2 in Physical AI
- Learn about nodes, DDS, and the system graph
- Explore the analogy of ROS 2 as a robotic nervous system

### Chapter 2: ROS 2 Communication
- Master nodes, topics, services, and actions
- Work with rclpy-based publisher/subscriber examples
- Understand data flow from sensors to actuators

### Chapter 3: Humanoid Modeling with URDF
- Learn URDF purpose and structure
- Understand links, joints, and frames
- Connect URDF to ROS 2 control systems

## Example Code Execution

Each chapter includes runnable examples. To run the examples:

1. Navigate to the examples directory for the chapter
2. Make sure your ROS 2 environment is sourced
3. Execute the example with the appropriate command

For Python examples:
```bash
python3 example_name.py
```

For more complex examples, follow the specific instructions in each chapter.

## Troubleshooting Common Issues

### Environment Not Sourced
If you get "command not found" errors for ROS 2 commands:
```bash
source /opt/ros/humble/setup.bash
```

### Permission Issues
If you encounter permission errors with colcon builds:
```bash
chmod +x ~/ros2_ws/install/setup.bash
```

### Network Configuration
For multi-machine communication, ensure ROS_DOMAIN_ID is consistent across machines:
```bash
export ROS_DOMAIN_ID=0
```

## Next Steps

1. Proceed to Chapter 1 to begin learning about ROS 2 fundamentals
2. Follow along with the examples to reinforce your understanding
3. Experiment with modifying the examples to deepen your knowledge

## Module-Specific Instructions

For this ROS 2 educational module:

1. **Start with the Docusaurus site**: Navigate to the AI-Book directory and start the development server:
   ```bash
   cd AI-Book
   npm start
   ```

2. **Access the Module**: The module will be available at [http://localhost:3000/docs/module-1-ros2](http://localhost:3000/docs/module-1-ros2)

3. **Work through the chapters in order**:
   - Chapter 1: ROS 2 Fundamentals
   - Chapter 2: ROS 2 Communication Patterns
   - Chapter 3: Humanoid Modeling with URDF

4. **Run the code examples**: Examples are located in `AI-Book/docs/module-1-ros2/examples/`
   - Simple publisher: `python3 simple-publisher.py`
   - Simple subscriber: `python3 simple-subscriber.py`
   - URDF model: `basic-urdf.urdf`

5. **Verify your understanding** with the self-assessment questions at the end of each chapter.