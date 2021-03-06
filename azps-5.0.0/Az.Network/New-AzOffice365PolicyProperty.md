---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 9fae8c6d543bddc3ad4110b95a1c1b4a1f146879
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323773"
---
# New-AzOffice365PolicyProperty

## SYNOPSIS
Sanal bir gereç sitesiyle kullanılmak üzere yeni bir Office 365 trafik kuralı belirtin.

## INDEKI

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
New-AzOffice365PolicyProperties komutu, sanal bir gereç sitesiyle kullanılacak bir Office 365 ayırıcı ilkesi tanımlar. 

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

Sanal Gereç sitesi komutlarıyla kullanılmak üzere Office 365 trafik ayırıcı ilke nesnesi oluşturun.

## PARAMETRELERINE

### -İzin ver
Kategori trafiğine izin ver 'i işaretleme.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Varsayılan
Varsayılan kategori trafiğini ayırıcılar.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -İyileştir
En İyileştir kategorisi trafiğini ayırıcılar.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSOffice365PolicyProperties

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
