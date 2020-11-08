---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AA58B897-EFA0-4321-9246-ED8E11AB3538
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a0e0d5cac7ac27bf7eeefe8e3eb995a82a32ea4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105982"
---
# New-AzureSSHKey

## SYNOPSIS
Var olan bir sertifikayı yeni Linux tabanlı bir Azure sanal makinelerine eklemek için bir SSH anahtar nesnesi oluşturur.

## INDEKI

### tuş çifti
```
New-AzureSSHKey [-KeyPair] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### PublicKey
```
New-AzureSSHKey [-PublicKey] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**New-AzureSSHKey** cmdlet 'i Azure 'a önceden eklenmiş bir SERTIFIKA Için SSH anahtar nesnesi oluşturur.
Bu SSH anahtar nesnesi, yeni- **AzureVM** kullanılarak yeni bir sanal makine için yapılandırma nesnesi oluştururken veya New- **Azutalep ickvm** ile yeni bir sanal makine oluştururken **Yeni-AzureProvisioningConfig** tarafından kullanılabilir.
Sanal makine oluşturma dosyasının bir parçası olarak dahil edildiğinde, belirtilen SSH ortak anahtarını veya anahtar çiftini yeni sanal makineye ekler.

## ÖRNEKLERDEN

### Örnek 1: sertifika ayar nesnesi oluşturma
```
PS C:\> $myLxCert = New-AzureSSHKey -Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
```

Bu komut, var olan sertifika için bir sertifika ayarı nesnesi oluşturur ve ardından nesneyi daha sonra kullanmak üzere bir değişkende depolar.

### Örnek 2: hizmete sertifika ekleme
```
PS C:\> Add-AzureCertificate -ServiceName "MySvc" -CertToDeploy "C:\temp\MyLxCert.cer"
$myLxCert = New-AzureSSHKey ?Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
New-AzureVMConfig -Name "MyVM2" -InstanceSize Small -ImageName $LxImage `
          | Add-AzureProvisioningConfig -Linux -LinuxUser $lxUser -SSHPublicKeys $myLxCert -Password 'pass@word1' `
          | New-AzureVM -ServiceName "MySvc"
```

Bu komut bir Azure hizmetine sertifika ekler ve ardından sertifikayı kullanan yeni bir Linux sanal makinesi oluşturur.

## PARAMETRELERINE

### -Parmak izi
Sertifikanın parmak izini belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

### -KeyPair
Bu cmdlet 'in yeni sanal makine yapılandırmasına SSH anahtar çiftini eklemek için bir nesne oluşturacağını belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: keypair
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Yol
SSH ortak anahtarının veya anahtar çiftinin depolanacağı yolu belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicKey
Bu cmdlet 'in yeni sanal makine yapılandırmasına SSH ortak anahtarı eklemek için bir nesne oluşturacağını belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: publickey
Aliases: 

Required: True
Position: 0
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

[Add-AzureProvisioningConfig](./Add-AzureProvisioningConfig.md)

[New-AzureVMConfig](./New-AzureVMConfig.md)

[New-AzureVM](./New-AzureVM.md)

[Yeni-Azutalep Ickvm](./New-AzureQuickVM.md)


