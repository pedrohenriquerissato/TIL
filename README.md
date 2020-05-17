# Today I Learned  

## 2020-05-17 - Create flutter app  
```bash
sudo git clone https://github.com/flutter/flutter.git -b stable /opt/flutter &&
sudo chown -R $USER:$USER /opt/flutter && 
echo "export PATH=\$PATH:/opt/flutter/bin" >> ~/.bashrc && 
source ~/.bashrc && 
flutter doctor
```
Resolve issues. 
Configure Android Studio >= 3.6:  
![](https://flutter.dev/assets/get-started/android/android-sdk-tools-7a3eaa161678e404dc0c570cc0f4921944a3413586bad47b5e1f585ddfefada0.png)  

Install Flutter extesion on VSCode then run on Command Palette:  
```vscode
> Flutter: Run Flutter Doctor
```  

Finnaly, run:
```bash
flutter create appname
cd appname  
flutter run
```