### **Liens**
- [Cybershoke](https://cybershoke.net/cs2)
- [CSFloat](https://csfloat.com/)

## **Optimisation des Performances – CS2 / Windows 11**

### **Options de Lancement CS2**
Utilisez ces paramètres pour optimiser le lancement du jeu :
```bash
+exec autoexec.cfg
```

---

## **Optimisation Windows 11**

### **1. Alimentation**
- **Plan d’alimentation** : *Performances élevées*

### **3. Mises à jour**
- **Désactiver** : Mises à jour automatiques des pilotes

### **4. Désactiver les Services Inutiles**

#### **Xbox Game Bar**
Exécutez ces commandes PowerShell :
```powershell
Get-AppxPackage *XboxGamingOverlay* | Remove-AppxPackage
Get-AppxPackage *XboxIdentityProvider* | Remove-AppxPackage
Get-AppxPackage *Xbox* | Remove-AppxPackage
```

#### **Game DVR (via Registre)**
```powershell
Set-ItemProperty -Path "HKCU:\System\GameConfigStore" -Name "GameDVR_Enabled" -Value 0 -Type DWord
```

#### **Services Liés (Optionnel)**
```powershell
Stop-Service -Name "XboxGipSvc" -Force
Set-Service -Name "XboxGipSvc" -StartupType Disabled
```

#### **Game Bar (via Paramètres Windows)**
```powershell
Set-ItemProperty -Path "HKCU:\Software\Microsoft\Windows\CurrentVersion\GameDVR" -Name "AppCaptureEnabled" -Value 0 -Type DWord
```

---

## **Options du Jeu – CS2**

### **Emplacement des Fichiers**
- **Autoexec** : `C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg`

### Audio Settings
- **Master Volume** 100
- **Main Menu Ambience Volume** 0
- **Audio Device:** DEFAULT DEVICE
- **EQ Profile:** CRISP
- **L/R Isolation:** 50%
- **Perspective Correction:** NO
- **Play Audio When Game in Background:** YES