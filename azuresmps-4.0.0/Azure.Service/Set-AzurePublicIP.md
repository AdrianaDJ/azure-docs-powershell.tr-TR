---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFD4E4AD-8F1B-4E4E-BF52-435A6EEAA060
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6beed021bfc12db3a3fdb1a66ee8ae6fe2e1e9b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105955"
---
# Set-AzurePublicIP

## SYNOPSIS
Azure sanal makinesine ortak IP ekler.

## INDEKI

```
Set-AzurePublicIP [-PublicIPName] <String> [[-IdleTimeoutInMinutes] <Int32>] [[-DomainNameLabel] <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**Set-AzurePublicIP** cmdlet 'ı bir Azure sanal MAKINESINE ortak IP ekler.
Var olan bir sanal makine için bu cmdlet 'i çalıştırırsanız, değişikliklerinizi uygulamak için sanal makineyi güncelleyin.
Genel IP için bir etki alanı adı etiketi belirtebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: var olan bir sanal makineye ortak IP ekleme
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" | Update-AzureVM
```

Bu komut, **Get-AzureVM** cmdlet 'Ini kullanarak Ftpınazure adlı hizmette ftpınstance adındaki sanal makineyi alır.
Komut, ardışık düzen işlecini kullanarak bu sanal makineyi geçerli cmdlet 'e geçirir.
Current cmdlet 'i, genel IP adı ftpıp adını ekler.
Komut, sanal makineyi değişikliklerinizi uygulayan **Update-AzureVM** cmdlet 'ine geçirir.

### Örnek 2: yeni bir sanal makineye ortak IP ekleme
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

Bu komut, **New-AzureVMConfig** cmdlet 'ini kullanarak bir sanal makine yapılandırma nesnesi oluşturur.
Komut bu nesneyi ek yapılandırma sağlayan **Add-AzureProvisioningConfig** cmdlet 'ine geçirir.
Current cmdlet 'i, genel IP adı ftpıp adını ekler.
Komut, yapılandırmayı sanal makineyi oluşturan **New-AzureVM** cmdlet 'ine geçirir.

### Örnek 3: var olan bir sanal makineye ortak IP ve etiket ekleme
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | Update-AzureVM
```

Bu komut, **Get-AzureVM** cmdlet 'Ini kullanarak Ftpınazure adlı hizmette ftpınstance adındaki sanal makineyi alır.
Komut, ardışık düzen işlecini kullanarak bu sanal makineyi geçerli cmdlet 'e geçirir.
Geçerli cmdlet, Public IP Name ftpıp adını ve adName etiketini ekler.
Komut değişikliklerinizi uygulayan sanal makineyi güncelleştirir.

### Örnek 4: yeni bir sanal makineye ortak IP ve etiket ekleme
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName $images[50].ImageName | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

Bu komut, bir sanal makine yapılandırma nesnesi oluşturur ve bu nesneyi ek yapılandırma sağlayan **Add-AzureProvisioningConfig** ile geçirir.
Geçerli cmdlet, Public IP Name ftpıp adını ve adName etiketini ekler.
Bu komut sanal makineyi oluşturur.

## PARAMETRELERINE

### -DomainNameLabel
Genel IP adresi için karşılık gelen DNS girdisinde kullanılacak adı belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Idfaizzamansayısı
TCP boşta kalma zaman aşımı süresini dakika olarak belirtir.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
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

### -PublicIPName
Genel IP adını belirtir.

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

### -VM
Bu cmdlet 'in genel IP 'yi eklediği sanal makineyi belirtir.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. Windowsaziy. Commands. ServiceManagement. model. IPersistentVM

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzurePublicIP](./Get-AzurePublicIP.md)

[Get-AzureVM](./Get-AzureVM.md)

[New-AzureVM](./New-AzureVM.md)

[New-AzureVMConfig](./New-AzureVMConfig.md)

[Remove-AzurePublicIP](./Remove-AzurePublicIP.md)

[Güncelleştirme-AzureVM](./Update-AzureVM.md)


