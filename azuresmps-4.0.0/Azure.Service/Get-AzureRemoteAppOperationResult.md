---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4136A0EF-2682-4B17-BC37-53CD43F5940B
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b884da0395313ddc8aa4d0e301b37849ec3d57
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106322"
---
# Get-AzureRemoteAppOperationResult

## SYNOPSIS
Azure RemoteApp işleminin sonucunu getirir.

## INDEKI

```
Get-AzureRemoteAppOperationResult [-TrackingId] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-AzureRemoteAppOperationResult** cmdlet 'i uzun süren bir Azure RemoteApp işlemi sonucunu alır.
Azure RemoteApp, hizmetin işlenmesi gereken birçok eylem için uzun süreli işlemler kullanır ve hemen geri dönemeyebilir.
İzleme kimliklerini döndüren cmdlet **örnekleri,** **Update-AzureRemoteAppCollection** , **set-azureremoteapp**

## ÖRNEKLERDEN

### Örnek 1: işlem sonucu almak için izleme KIMLIĞI kullanma
```
PS C:\> $result = New-AzureRemoteAppCollection -CollectionName Contoso -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
PS C:\> Get-AzureRemoteAppOperationResult -TrackingId $result.Tracking
```

Bu komut, bir Azure RemoteApp işleminden döndürülen izleme KIMLIĞINI kaydeder.
İzleme KIMLIĞI, aşağıdaki komutta, **Get-Azureremoteappoperation'** a geçirilir.

## PARAMETRELERINE

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

### -Trackingıd
İşlemin izleme KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Bağlantısı kesiliyor-AzureRemoteAppSession](./Disconnect-AzureRemoteAppSession.md)

[Set-AzureRemoteAppWorkspace](./Set-AzureRemoteAppWorkspace.md)

[Update-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


