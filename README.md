# Setup certificates, provisioning profiles to develop iOS on multiple machines/computers

## 1. Create .certSigningRequest

### 1.1 Open Keychain Access

### 1.2 Select Keychain Access > Certificate Assistant > Request a Certificate From a Certificate Authority…
![](images/img_01.png)

### 1.3 Enter email, name & click Continue
![](images/img_02.png)

### 1.4 Save file .certSigningRequest
![](images/img_03.png)



## 2. Create Apple Development/Distribution certificate

### 2.1 Go to https://developer.apple.com/account/resources/certificates/list

### 2.2 Add certificate by click to button add (+)
![](images/img_04.png)

### 2.3 Choose Apple Development/Apple Distribution & click Continue
![](images/img_05.png)

### 2.4 Choose file .certSigningRequest (in Step 1.4)
![](images/img_06.png)

### 2.5 Download Development/Distribution certificate (file .cer)
![](images/img_07.png)

### 2.6 Double click to certificate to add to your keychain
![](images/img_08.png)



## 3. Create development/distribution provisioning profile

### 3.1 Open https://developer.apple.com/account/resources/profiles/list

### 3.2 Add profile by click button add (+)
![](images/img_09.png)

### 3.3 Choose iOS App Development (or App Store) & click Continue
![](images/img_10.png)

### 3.4 Select your app ID from dropdown & click Continue
![](images/img_11.png)

### 3.5 Select certificates & click Continue
![](images/img_12.png)

### 3.6 Select devices & click Continue (optional)
![](images/img_13.png)

### 3.7 Enter provisioning profile name & click Generate
![](images/img_14.png)

### 3.8 Download provisioning profile (file .mobileprovision)
![](images/img_15.png)

### 3.9 Open project by XCode

### 3.10 Import Development/Distribution .mobileprovision to your project
![](images/img_16.png)


#### Note
- It may not work on the first time, quit Xcode & reopen project

#### Congratulation:
- You're done. From now, you can build & distribute iOS app on your own machine
- To develop on another machines, you need to do one more step



## 4. Export your certificates to develop on multiple machines

### 4.1 Open Keychain Access && enter “apple” in search box

### 4.2 Search installed certificates
![](images/img_17.png)

#### Note
- Certificate must contain private key && Name of private key must be the same with name in Step 1.3

### 4.3 Export Development/Distribution certificates
![](images/img_18.png)

### 4.4 Choose format: Personal Information Exchange .p12 & save
![](images/img_19.png)

#### Note
- Other file formats will not work as expected

### 4.5 Done: Send files (.p12 & .mobileprovision) to another computer & work
![](images/img_20.png)

#### Congratulation: Everything done 🎉🎉🎉
