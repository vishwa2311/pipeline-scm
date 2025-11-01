pipeline {
  agent any
  stages {
    stage('System Info') {
      steps {
        sh '''
          echo "=== Project 2: System Info ==="
          echo "Computer Name: $(hostname)"
          echo "User: $(whoami)"
          echo "Kernel: $(uname -r)"
          # OS information (works on most Linux distros)
          if [ -f /etc/os-release ]; then
            . /etc/os-release
            echo "OS Name: $NAME"
            echo "OS Version: $VERSION"
          else
            echo "OS info file not found, trying lsb_release..."
            lsb_release -a 2>/dev/null || echo "lsb_release not available"
          fi
          echo "Uptime: $(uptime -p)"
        '''
      }
    }
  }
}
