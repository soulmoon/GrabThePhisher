# 🐟 GrabThePhisher Lab Report  

## 📂 Category  
- Threat Intel  

## 🎯 Tactics  
- Initial Access  
- Exfiltration  

## 🛠️ Tool  
- Text Editor  

---

## 📖 Scenario  
A decentralized finance (DeFi) platform recently reported multiple user complaints about **unauthorized fund withdrawals**.  
A forensic review uncovered a **phishing site impersonating the PancakeSwap exchange**, luring victims into entering their wallet seed phrases.  

The phishing kit was hosted on a compromised server and exfiltrated credentials via a **Telegram bot**.  
Your task: conduct **threat intelligence analysis** on the phishing infrastructure, identify **indicators of compromise (IoCs)**, and track the attacker’s **online presence** including aliases and Telegram identifiers, to understand their **TTPs**.  

---

## 📝 Questions & Answers  

**Q1. Which wallet is used for asking the seed phrase?**  
✅ MetaMask  
<img width="940" height="667" alt="image" src="https://github.com/user-attachments/assets/ebe842cb-915a-436d-96b5-32e2fd007a27" />

**Q2. What is the file name that has the code for the phishing kit?**  
✅ metamask.php  
<img width="940" height="927" alt="image" src="https://github.com/user-attachments/assets/5a0d738e-2d67-4105-9ec7-3996c2537ea2" />

**Q3. In which language was the kit written?**  
✅ PHP  

**Q4. What service does the kit use to retrieve the victim's machine information?**  
✅ Sypex Geo  
<img width="940" height="693" alt="image" src="https://github.com/user-attachments/assets/bc80a7f5-c5fc-4b51-b738-4b8af4094cb1" />

**Q5. How many seed phrases were already collected?**  
✅ 3  
<img width="934" height="378" alt="image" src="https://github.com/user-attachments/assets/59fad749-8daf-4334-9ab6-683b8bbc8576" />

**Q6. Provide the seed phrase associated with the most recent phishing incident.**  
✅ `father also recycle embody balance concert mechanic believe owner pair muffin hockey`  
<img width="934" height="378" alt="image" src="https://github.com/user-attachments/assets/f80ce7b1-c18f-4f4e-acb1-22594ca31592" />

**Q7. Which medium was used for credential dumping?**  
✅ Telegram  
<img width="940" height="115" alt="image" src="https://github.com/user-attachments/assets/0c77f366-ef82-440b-b37e-d35e7b407787" />

**Q8. What is the token for accessing the channel?**  
✅ `5457463144:AAG8t4k7e2ew3tTi0IBShcWbSia0Irvxm10`  
<img width="940" height="157" alt="image" src="https://github.com/user-attachments/assets/4921c774-9d34-4f65-9f85-5813b7404139" />

**Q9. What is the Chat ID for the phisher's channel?**  
✅ `5442785564`  
<img width="940" height="171" alt="image" src="https://github.com/user-attachments/assets/1331587a-3c5d-4f93-9c96-959e28b0820f" />

**Q10. What are the allies of the phish kit developer?**  
✅ `j1j1b1s@m3r0`  
<img width="895" height="442" alt="image" src="https://github.com/user-attachments/assets/1567a726-b388-466c-a5d6-8604ba06e141" />

**Q11. What is the full name of the Phish Actor?**  
✅ Marcus Aurelius  
curl -X POST -H "Content-Type: application/json" -d '{"chat_id":"5442785564"}' https://api.telegram.org/bot5457463144:AAG8t4k7e2ew3tTi0IBShcWbSia0Irvxm10/getChat
<img width="940" height="115" alt="image" src="https://github.com/user-attachments/assets/37be8fd8-f9c6-408e-ac2e-ae461552d11c" />

**Q12. What is the username of the Phish Actor?**  
✅ pumpkinboii  
curl -X POST -H "Content-Type: application/json" -d '{"chat_id":"5442785564"}' https://api.telegram.org/bot5457463144:AAG8t4k7e2ew3tTi0IBShcWbSia0Irvxm10/getChat
<img width="940" height="115" alt="image" src="https://github.com/user-attachments/assets/b21ad1c9-8354-47cc-a620-e0d62559aaa7" />

---

## 🔑 Key Findings  

- 🎯 **Targeted Wallet**: MetaMask users  
- 💻 **Phishing Kit File**: `metamask.php` (written in PHP)  
- 🌍 **Victim Info Collection**: via **Sypex Geo API**  
- 🛑 **Collected Seed Phrases**: 3 (latest phrase exfiltrated)  
- 📡 **Exfiltration Channel**: Telegram bot  
- 🔐 **Telegram Bot Token**: `5457463144:AAG8t4k7e2ew3tTi0IBShcWbSia0Irvxm10`  
- 📲 **Telegram Chat ID**: `5442785564`  
- 👥 **Allies**: `j1j1b1s@m3r0`  
- 🕵️ **Phish Actor Identity**: Marcus Aurelius (**@pumpkinboii**)  

---

## 📌 Conclusion  
This investigation highlights how attackers leveraged a **phishing kit** targeting MetaMask users to exfiltrate sensitive wallet recovery phrases.  
The kit was **PHP-based**, collected **3 seed phrases**, and transmitted stolen credentials through **Telegram**.  

Key attribution was possible through the analysis of the kit’s configuration files, which exposed the attacker’s **Telegram token, chat ID, and aliases**. The identified actor, **Marcus Aurelius (@pumpkinboii)**, appears to have **collaborators** and continues leveraging phishing infrastructure for credential theft.  

⚠️ **Defenders should monitor IoCs, block Telegram exfiltration channels, and educate users on phishing awareness to prevent credential compromise.**  
