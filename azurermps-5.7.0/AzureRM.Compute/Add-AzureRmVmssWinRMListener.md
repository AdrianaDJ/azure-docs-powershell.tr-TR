---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
ms.openlocfilehash: d2ed576131ad2ff33ae7e5c7e5be091ca8f4a50e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586809"
---
# Add-AzureRmVmssWinRMListener

## SYNOPSIS
VMSS 'ye WinRM dinleyicisi ekler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Add-AzureRmVmssWinRMListener** cmdlet 'ı, sanal makine ölçek kümesinde (VMSS) Windows Uzaktan Yönetim (WinRM) dinleyicisi ekler.

## ÖRNEKLERDEN

### Örnek 1: VMSS 'ye WinRM dinleyicisi ekleme
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

Bu örnek, VMSS 'ye bir WinRM dinleyicisi ekler.

İlk komut, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzureRmVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.
İkinci komut, belirtilen URL 'deki sertifikayı VMSS 'ye içeren bir HTTP protokolü WinRM dinleyicisi ekler.

## PARAMETRELERINE

### -CertificateUrl 'Si
Yeni sanal makinelerin sağlandığı sertifikanın URL 'sini içeren bir bağlantı belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -İletişim kuralı
WinRM dinleyicisi protokolünü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Http
- Https

```yaml
Type: ProtocolTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
VMSS nesnesini belirtir.
Nesneyi oluşturmak için New-AzureRmVmssConfig cmdlet 'ini kullanabilirsiniz.

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Bu cmdlet hiçbir çıkış üretmez.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzureRmVmssConfig](./New-AzureRmVmssConfig.md)


