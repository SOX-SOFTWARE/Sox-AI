# Sox-AI
SOX AI is a futuristic personal AI assistant designed to bring intelligent conversations, voice interaction, cinematic animations, and personalized device control to Windows and Android. Featuring customizable AI models, API keys, themes, moods, and a sleek sci-fi interface, SOX AI aims to make everyday computing smarter, simpler, and more personal
How To Dowload 
.Extract The Dowloaded File 
.Then Open .bat file and wait for finishing the dowloads 
.Then Enjoy........
SOX AI 🚀
A cross-platform personal AI assistant designed to handle tasks across Windows and mobile, chat naturally, and keep things looking slick with a smooth, cinematic interface.

What's inside?
Cinematic UI: Built with fluid animations and a modern dark aesthetic so it actually feels fun and futuristic to use.

Dynamic Moods: You can easily switch how the AI behaves and responds depending on your vibe (whether you want it casual, professional, or direct).

One-Click Windows Launcher: No need to manually mess around with terminal commands every time. The setup script handles everything automatically.

Local Settings: Keep your custom API keys and themes managed locally and securely.

Quick Start (Windows)
Getting things running on Windows is super simple. Just clone the repo and use the included launcher script (run_sox.bat).

The script automatically checks for Python, sets up your virtual environment (.venv), installs the required dependencies from requirements.txt, and boots up the app:

Code snippet
@echo off
title SOX AI - Personal Assistant Launcher
echo ========================================================
echo               SOX AI Windows Desktop Edition
echo ========================================================
echo.

where python >nul 2>nul
if %ERRORLEVEL% neq 0 (
    echo [ERROR] Python is not installed or not in PATH!
    echo Please install Python 3.12+ from https://www.python.org/
    echo Make sure to check "Add Python to PATH" during installation.
    pause
    exit /b 1
)

if not exist ".venv" (
    echo [1/3] Creating Python Virtual Environment...
    python -m venv .venv
)

echo [2/3] Activating environment and checking dependencies...
call .venv\Scripts\activate.bat

echo [3/3] Installing/verifying requirements...
pip install -r requirements.txt --quiet

echo.
echo Starting SOX AI...
python sox_ai_app.py

pause
