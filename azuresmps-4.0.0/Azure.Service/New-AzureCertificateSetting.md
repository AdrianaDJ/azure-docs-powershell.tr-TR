---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 11919623-9EDF-42A3-93FE-54E93D76D3D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7492dbdea0f924e364ac1acf5ce30476e34782d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105932"
---
# New-AzureCertificateSetting

## SYNOPSIS
Sertifika için sertifika ayarı nesnesi oluşturur.

## INDEKI

```
New-AzureCertificateSetting [[-StoreName] <String>] [-Thumbprint] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**New-Azurecercertificate Atesetting** cmdlet 'ı, Azure hizmetinde bulunan bir sertifika için sertifika ayarı nesnesi oluşturur.

**Add-AzureProvisioningConfig** cmdlet 'ini kullanarak yapılandırma nesnesi oluşturmak için sertifika ayarı nesnesini kullanabilirsiniz.
**New-AzureVM** cmdlet 'ini kullanarak sanal makine oluşturmak için yapılandırma nesnesi kullanın.
**Yeni-Azutalep Ickvm** cmdlet 'ini kullanarak sanal makine oluşturmak için sertifika ayarı nesnesi kullanabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: sertifika ayar nesnesi oluşturma
```
PS C:\> New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My"
```

Bu komut, var olan bir sertifika için sertifika ayarı nesnesi oluşturur.

### Örnek 2: yapılandırma ayarı nesnesini kullanan bir sanal makine oluşturma
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy "C:\temp\ContosoCert.cer"
PS C:\> $CertificateSetting = New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My" 
PS C:\> $Image = Get-AzureVMImage -ImageName "ContosoStandard"
PS C:\> New-AzureVMConfig -Name "VirtualMachine17" -InstanceSize Small -ImageName $Image | Add-AzureProvisioningConfig -Windows -Certificates $CertificateSetting -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

İlk komut, **Add-Azurecercertificate** . cer 'i kullanarak, contosocert. cer ' i contosohizmeti adlı hizmete ekler.

İkinci komut bir sertifika ayarı nesnesi oluşturur ve $CertificateSetting değişkeninde depolar.

Üçüncü komut, **Get-AzureVMImage** cmdlet 'ini kullanarak görüntü deposundaki bir resmi alır.
Bu komut, resmi $Image değişkeninde depolar.

Son komutu, **Yeni-AzureVMConfig** cmdlet 'ini kullanarak $Image resim temelinde bir sanal makine yapılandırma nesnesi oluşturur.
Komut, bu nesneyi ardışık düzen işlecini kullanarak **Add-AzureProvisioningConfig** cmdlet 'ine geçirir.
Bu cmdlet, yapılandırma bilgilerini yapılandırmaya ekler.
Komut, nesneyi sanal makineyi oluşturan **New-AzureVM** cmdlet 'ine geçirir.

## PARAMETRELERINE

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

### -StoreName
Sertifikanın yerleştirileceği sertifika deposunu belirtir.
Geçerli değerler: 

- Adres defteri
- AuthRoot
- CertificateAuthority
- Verilemeyen
- Bilgilerimi
- Kökü
- Trustedkişilerim
- TrustedPublisher

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azurecercertificate](./Add-AzureCertificate.md)

[Add-AzureProvisioningConfig](./Add-AzureProvisioningConfig.md)

[Get-Azurecercertificate](./Get-AzureCertificate.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Yeni-Azutalep Ickvm](./New-AzureQuickVM.md)

[New-AzureVM](./New-AzureVM.md)

[Remove-Azurecercertificate](./Remove-AzureCertificate.md)


