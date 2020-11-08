---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9FCECA04-9855-461C-9470-85312993C4B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bb7bb3e708720b481edc4489d858c70736eac95
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106026"
---
# Start-AzureVNetGatewayDiagnostics

## SYNOPSIS
VPN ağ geçidi için ağ geçidi tanılaması başlatır.

## INDEKI

```
Start-AzureVNetGatewayDiagnostics -VNetName <String> -CaptureDurationInSeconds <Int32>
 [-ContainerName <String>] -StorageContext <AzureStorageContext> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Start-AzureVNetGatewayDiagnostics** cmdlet 'i sanal özel ağ (VPN) ağ geçidi için yeni bir ağ geçidi tanılama oturumu başlatır.
Aynı anda yalnızca bir ağ geçidi tanılama oturumu çalıştırılabilir.
Ağ geçidi tanılama oturumu çalışırken bu cmdlet 'i çalıştırırsanız, bu cmdlet bir hata döndürür.

## ÖRNEKLERDEN

## PARAMETRELERINE

### -CaptureDurationInSeconds
Yakalama süresini saniye cinsinden belirtir.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kapsayıcıadı
Bir Azure kapsayıcısının adını belirtir.
Bu cmdlet sonuçları bu parametrenin belirttiği kapsayıcıda depolar.

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
Bu cmdlet 'in okuduğu Azure profilini belirtir. Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

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

### -StorageContext
Azure depolama bağlamını belirtir.
Bu cmdlet, bu parametrenin belirttiği depolama bağlamını kullanarak sonuçları depolar.

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vağ adı
Bu cmdlet 'in tanılama çalıştırdığı sanal ağ geçidi içeren sanal ağı belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

[Get-AzureVNetGatewayDiagnostics](./Get-AzureVNetGatewayDiagnostics.md)

[Stop-AzureVNetGatewayDiagnostics](./Stop-AzureVNetGatewayDiagnostics.md)


