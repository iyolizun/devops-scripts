#!/usr/bin/env python3
import os

def check_script_status():
    """Check if the script is running or not."""
    script_name = 'devops-scripts'
    process_name = 'python -m devops-scripts.run'
    
    # Get the list of process names
    processes = [p.info['name'] for p in os.listdir('/proc')]
    
    # Check if the process is running
    if process_name in processes:
        return True
    else:
        return False

if __name__ == '__main__':
    print(check_script_status())