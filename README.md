# 🧠 RL DQN Agent for Hangman

## 📜 Overview
This project implements a **Deep Q-Network (DQN)**–based Reinforcement Learning agent to play the classic **Hangman** word-guessing game.  
The notebook demonstrates how an RL agent can learn optimal letter-guessing strategies through interaction and reward feedback instead of hardcoded heuristics.

---

## ⚙️ Features
- **DQN implementation using PyTorch**
- **Custom Hangman environment**
- **Experience replay and epsilon-greedy exploration**
- **Support for adjustable game parameters (word length, max lives, etc.)**
- **Training and evaluation routines**
- **Corpus-based vocabulary loading**

---

## 🧩 Project Structure
```
ml-hackathon-hmm.ipynb   # Main Jupyter Notebook (core implementation)
corpus.txt                # Word dataset file (required)
```

---

## 🧠 How It Works
1. **Environment Setup** – The agent interacts with a Hangman environment that provides state feedback after each letter guess.  
2. **State Representation** – Each game state encodes known letters, guesses, and remaining lives.  
3. **Action Space** – The 26 English alphabet letters.  
4. **Reward Signal** – Positive reward for correct guesses, negative for incorrect, and terminal penalties for losing.  
5. **DQN Agent** – A neural network approximates the Q-value function.  
6. **Training Loop** – The agent improves by playing thousands of episodes, updating the network using replay memory.

---

## 🧰 Requirements
Install the following before running:
```bash
pip install torch numpy matplotlib tqdm
```

---

## 🚀 Usage
1. Clone or download the project.  
2. Ensure `corpus.txt` is in the same folder as the notebook.  
3. Open the notebook:
   ```bash
   jupyter notebook ml-hackathon-hmm.ipynb
   ```
4. Run all cells to train and test the DQN agent.

---

## 📈 Evaluation
The notebook includes an evaluation method that tests the trained model across multiple episodes and measures:
- Average reward per episode  
- Win rate  
- Guess accuracy  

---

## ⚠️ Limitations
- Requires a sufficiently large training set to generalize.  
- DQN may overfit short or repetitive words.  
- Slow training if GPU (CUDA) isn’t available.  
- Limited exploration efficiency due to static epsilon decay.

---

## 🧑‍💻 Authors
Developed for an **ML Hackathon** exploring RL-based approaches to symbolic reasoning and word games.
- PES1UG23AM360
- PES1UG23AM314
- PES1UG23AM353
- PES1UG23AM352