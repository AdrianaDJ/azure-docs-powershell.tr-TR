---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0B3EF123-8424-4CCA-95E8-01301B70CBDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84db81f51a4f8d0da605917f99e14c1721cd89d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106382"
---
# Add-AzureProvisioningConfig

## SYNOPSIS
Azure sanal makinesi için sağlama yapılandırması ekler.

## INDEKI

### Windows (varsayılan)
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>] [-Windows]
 [-AdminUsername <String>] [-Password <String>] [-ResetPasswordOnFirstLogon] [-DisableAutomaticUpdates]
 [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>] [-EnableWinRMHttp]
 [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>]
 [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### UX
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-Linux] [-LinuxUser <String>]
 [-DisableSSH] [-NoSSHEndpoint] [-NoSSHPassword] [-SSHPublicKeys <SSHPublicKeyList>]
 [-SSHKeyPairs <SSHKeyPairList>] [-CustomDataFile <String>] [-Password <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### WindowsDomain
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>]
 -AdminUsername <String> [-WindowsDomain] [-Password <String>] [-ResetPasswordOnFirstLogon]
 [-DisableAutomaticUpdates] [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>]
 -JoinDomain <String> -Domain <String> -DomainUserName <String> -DomainPassword <String>
 [-MachineObjectOU <String>] [-EnableWinRMHttp] [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>]
 [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**Add-AzureProvisioningConfig** cmdlet 'ı bir Azure sanal makine yapılandırmasına sağlama yapılandırma bilgilerini ekler.
Sanal makine oluşturmak için yapılandırma nesnesini kullanabilirsiniz.

Bu cmdlet tek başına Windows sunucuları, Active Directory etki alanına bağlı Windows sunucuları ve Linux tabanlı sunucular gibi farklı sağlama yapılandırmalarını destekler.

Active Directory etki alanı Birleşik sunucusu oluşturmak için, Active Directory etki alanının tam etki alanı adını ve sanal makineye etki alanına katılma izni olan bir kullanıcının etki alanı kimlik bilgilerini belirtin.

## ÖRNEKLERDEN

### Örnek 1: tek başına sanal makine oluşturma
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService"
```

Bu komut, **New-AzureVMConfig** cmdlet 'ini kullanarak bir sanal makine yapılandırma nesnesi oluşturur.
Komut, ardışık düzen işlecini kullanarak nesneyi geçerli cmdlet 'e geçirir.
Geçerli cmdlet, Windows işletim sistemini çalıştıran bir sanal makine için sağlama yapılandırması ekler.
Yapılandırma, yönetici kullanıcı adını ve parolasını içerir.
Komut, yapılandırmayı sanal makineyi oluşturan **New-AzureVM** cmdlet 'ine geçirir.

### Örnek 2: etki alanına bağlı bir sanal makine oluşturma
```
PS C:\> New-AzureVMConfig -Name "DomainVM" -InstanceSize Small -ImageName "Image09" | Add-AzureProvisioningConfig -WindowsDomain -Password "password" -AdminUsername "AdminMain" -ResetPasswordOnFirstLogon -JoinDomain "contoso.com" -Domain "contoso" -DomainUserName "DomainAdminUser" -DomainPassword "DomainPassword" -MachineObjectOU 'OU=AzureVMs,DC=contoso,DC=com' | New-AzureVM -ServiceName "ContosoService"
```

Bu komut bir sanal makine yapılandırma nesnesi oluşturur ve bunu geçerli cmdlet 'e geçirir.
Geçerli cmdlet, contoso etki alanına katılması için bir sanal makinenin sağlama yapılandırmasını ekler.
Bu komut, sanal makineye etki alanına katılmak için gereken kullanıcı adını ve parolayı içerir.
Yapılandırma, kullanıcının ilk oturum açmada Kullanıcı parolasını değiştirmesini gerektirir.
Bu komut, hazırlama nesnesini temel alarak sanal makineyi oluşturur.

### Örnek 3: Linux tabanlı sanal makine oluşturma
```
PS C:\> New-AzureVMConfig -Name "LinuxVM" -InstanceSize Small -ImageName "LinuxImage03" | Add-AzureProvisioningConfig -Linux -LinuxUser "LinuxRoot" -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

Bu komut bir sanal makine yapılandırma nesnesi oluşturur ve bunu geçerli cmdlet 'e geçirir.
Geçerli cmdlet, Linux işletim sistemini çalıştıran bir sanal makine için sağlama yapılandırması ekler.
Yapılandırma, kök kullanıcı adını ve parolasını içerir.
Bu komut, hazırlama nesnesini temel alarak sanal makineyi oluşturur.

### Örnek 4: WinRM için sertifikaları içeren bir sanal makine oluşturma
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image11" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

İlk komut sertifika deposundaki sertifikaları alır ve bunları $certs dizi değişkeninde depolar.

İkinci komut bir sanal makine yapılandırma nesnesi oluşturur ve bunu geçerli cmdlet 'e geçirir.
Geçerli cmdlet, WinRM için sertifikaları içeren sağlama yapılandırması ekler.
Bu komut, hazırlama nesnesini temel alarak sanal makineyi oluşturur.

### Örnek 5: HTTP üzerinden WinRM 'ye sahip bir sanal makine oluşturma
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image14" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -EnableWinRMHttp | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Bu komut bir sanal makine yapılandırma nesnesi oluşturur ve bunu geçerli cmdlet 'e geçirir.
Geçerli cmdlet, HTTP üzerinden WinRM 'ye sahip sağlama yapılandırması ekler.
Bu komut, hazırlama nesnesini temel alarak sanal makineyi oluşturur.

### Örnek 6: WinRM HTTPS üzerinden devre dışı bırakılmış bir sanal makine oluşturma
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -DisableWinRMHttps | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Bu komut bir sanal makine yapılandırma nesnesi oluşturur ve bunu geçerli cmdlet 'e geçirir.
Geçerli cmdlet, HTTPS üzerinden WinRM 'yi devre dışı bırakan sağlama yapılandırması ekler.
Bu komut, hazırlama nesnesini temel alarak sanal makineyi oluşturur.

### Örnek 7: anahtar dışarı aktarma olmadan sanal makine oluşturma
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -X509Certificates $certs[0], $certs[1] -NoExportPrivateKey | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

İlk komut sertifika deposundaki sertifikaları alır ve bunları $certs dizi değişkeninde depolar.

İkinci komut bir sanal makine yapılandırma nesnesi oluşturur ve bunu geçerli cmdlet 'e geçirir.
Geçerli cmdlet, sertifikaları içeren ve özel anahtarları dışarı aktarmaz bir sanal makine için sağlama yapılandırması ekler.
Bu komut, hazırlama nesnesini temel alarak sanal makineyi oluşturur.

## PARAMETRELERINE

### -AdminUsername
Bu yapılandırmanın sanal makinede oluşturduğu yönetici hesabının kullanıcı adını belirtir.

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sertifikalar
Bu yapılandırmanın sanal makinede yüklediği sertifika kümesini belirtir.

```yaml
Type: CertificateSettingList
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Customveri dosyası
Sanal makine için bir veri dosyası belirtir.
Bu cmdlet, dosyanın içeriğini Base64 olarak kodlar.
Dosya 64 kilobayt uzunluğundan az olmalıdır.

Konuk işletim sistemi Windows işletim sistemdeydi, bu yapılandırma bu verileri%SYSTEMDRIVE%\AzureData\CustomData.bin. adlı bir ikili dosya olarak kaydeder.

Konuk işletim sistemi Linux ise, bu yapılandırma ovf-env.xml dosyasını kullanarak verileri geçirir.
Yapılandırma, dosyayı/var/lib/waagent dizinine kopyalar.
Aracı Ayrıca,/var/lib/waagent/customdata'de Base64 Ile kodlanmış verileri depolar.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableAutomaticUpdates
Bu yapılandırmanın otomatik güncelleştirmeleri devre dışı bırakacağını gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableGuestAgent
Bu yapılandırmanın, altyapıyı bir hizmet (IaaS) Konuk Aracısı olarak devre dışı bırakacağını gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableSSH
Bu yapılandırmanın, SSH 'in devre dışı olduğunu gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWinRMHttps
Bu yapılandırmanın HTTPS üzerinde Windows Uzaktan Yönetimi 'ni (WinRM) devre dışı bırakacağını gösterir.
Varsayılan olarak, HTTPS HTTPS üzerinden etkinleştirilir.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Etki alanı
Bilgisayarı etki alanına ekleme izni olan hesabın etki alanı adını belirtir.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainPassword
Bilgisayarı etki alanına ekleme iznine sahip olan kullanıcı hesabının parolasını belirtir.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainUserName
Bilgisayarı etki alanına ekleme iznine sahip olan kullanıcı hesabının adını belirtir.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWinRMHttp
Bu yapılandırmanın HTTP üzerinden WinRM 'yi etkinleştirdiğini belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Informationaction
Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.

Bu parametre için kabul edilebilir değerler şunlardır:

- 'A
- Manıza
- Sorgulamak
- Sustlıkdevam
- Durdurduğunuzda
- Biliriz

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Informationvariable
Bir bilgi değişkeni belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JoinDomain
Katılacak etki alanının tam etki alanı adını (FQDN) belirtir.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Linux
Bu yapılandırmanın bir Linux yapılandırması oluşturduğunu gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LinuxUser
Bu yapılandırmanın sanal makinede oluşturduğu Linux yönetim hesabının kullanıcı adını belirtir.

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MachineObjectOU
Yapılandırma bilgisayar hesabını oluştururken kuruluş biriminin (OU) tam nitelikli adını belirtir.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoExportPrivateKey
Bu yapılandırmanın özel anahtarı yükleymediğini belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoRDPEndpoint
Bu yapılandırmanın uzak masaüstü uç noktası olmadan bir sanal makine oluşturacağını gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoSSHEndpoint
Bu yapılandırmanın, SSH uç noktası olmadan bir sanal makine oluşturduğunu gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoSSHPassword
Bu yapılandırmanın, SSH parolası olmadan bir sanal makine oluşturduğunu gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nowinrmenvseçnokta
Bu yapılandırmanın sanal makine için WinRM uç noktası eklemediğini gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Parola
Yönetici hesabının parolasını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResetPasswordOnFirstLogon
Sanal makinenin, kullanıcının ilk oturum açmada parolasını değiştirmesini gerektirdiğini belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHKeyPairs
SSH anahtar çiftlerini belirtir.

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHPublicKeys
SSH ortak anahtarlarını belirtir.

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeZone
Sanal makinenin saat dilimini (örneğin, Pasifik standart saati veya Kanada Merkezi Standart Saati) belirtir.

```yaml
Type: String
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Bir sanal makine nesnesi belirtir.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Windows
Bu yapılandırmanın, Windows işletim sistemini çalıştıran tek başına bir sanal makine oluşturduğunu gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WindowsDomain
Bu yapılandırmanın, Active Directory etki alanına bağlı Windows Server 'ı oluşturduğunu gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Winrmcercertificate
Bu yapılandırmanın WinRM uç noktasıyla ilişkilendiğinde bir sertifika belirtir.

```yaml
Type: X509Certificate2
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -X509Certificates
Barındırılan bir hizmete dağıtılan x509 sertifikalarının dizisini belirtir.

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureVM](./New-AzureVM.md)

[New-AzureVMConfig](./New-AzureVMConfig.md)


