pipeline {
agent any
stages {
stage('System Info') {
steps {
bat """
@echo off
echo === Project 2: System Info ===
echo Computer Name: %COMPUTERNAME%
echo User: %USERNAME%
ver
systeminfo | findstr /B /C:"OS Name" /C:"OS
Version"
"""
}
}
}
}
