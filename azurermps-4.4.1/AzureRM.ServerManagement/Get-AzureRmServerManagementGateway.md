---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: C579BF90-FD8B-4384-96EB-46154E308492
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
ms.openlocfilehash: 6b98f4266e730e1cfb60ef51046e6846f24999d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762691"
---
# Get-AzureRmServerManagementGateway

## SYNOPSIS
Bir veya daha fazla sunucu yönetimi ağ geçidi alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### NoParams (varsayılan)
```
Get-AzureRmServerManagementGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Many-ByResourceGroup
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Single-ByName
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Single-ByObject
```
Get-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureRmServerManagementGateway** cmdlet 'i bir veya daha fazla Azure Server Management Gateway alır.

## ÖRNEKLERDEN

### Örnek 1: abonelikteki tüm ağ geçitlerini alma
```
PS C:\>Get-AzureRmServerManagementGateway
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
groupOne       centralus      Off          mygateway
groupOne       centralus      Off          othergateway
groupTwo       centralus      On           privategateway
```

Bu komut, abonelikteki tüm sunucu yönetimi ağ geçitlerini alır.

### Örnek 2: kaynak grubundaki ağ geçitlerini alma
```
PS C:\>Get-AzureRmServerManagementGateway -ResourceGroupName "Group001"
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
myGroup        centralus      Off          mygateway
```

Bu komut, Group001 adlı kaynak grubuna ait olan tüm sunucu yönetimi ağ geçitlerini alır.

### Örnek 3: bir ağ geçidinin tüm yüklü örneklerini alma
```
PS C:\>(Get-AzureRmServerManagementGateway -ResourceGroupName "Group002" -GatewayName "Gateway01").Instances
Name             Installed              Version         Operating System
----             ---------              -------         ----------------
GATEWAYPC        4/13/2016 6:35:04 PM   1.0.1104.0      Microsoft Windows 10 Enterprise
```

Bu komut, Group002 adındaki kaynak grubuna ait olan Gateway01 adındaki bir sunucu yönetimi ağ geçidinin tüm örneklerini alır.

## PARAMETRELERINE

### -Ağ Geçidi
Bu cmdlet 'in aldığı ağ geçidini belirtir.

Cmdlet, eylemi gerçekleştirmek için belirtilen ağ geçidi aracılığıyla *Resourcegroupname* ve *GatewayName* parametrelerini kullanır.

Bu parametre belirtildiğinde, bu cmdlet ağ geçidi için ayrıntılı durumu içerir.

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: Single-ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -GatewayName
Bu cmdlet 'in kapısı aldığı sunucu yönetimi ağ geçidinin adını belirtir.

*GatewayName* parametresini belirttiğinizde, bu cmdlet ağ geçidinde ayrıntılı durumu içerir.

```yaml
Type: System.String
Parameter Sets: Single-ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet ağ geçitleri aldığı kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: Many-ByResourceGroup, Single-ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Geçidi
' Ağ Geçidi ' parametresi ardışık düzenin ' Gateway ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Azure. Commands. ServerManagement. model. geçit

## NOTLARıNDA
* Bu cmdlet parametre olmadan kullanıyorsanız, abonelikle ilişkilendirilmiş tüm ağ geçitleri döner.

## ILGILI BAĞLANTıLAR

[Yeni-AzureRmServerManagementGateway](./New-AzureRmServerManagementGateway.md)

[Remove-AzureRmServerManagementGateway](./Remove-AzureRmServerManagementGateway.md)


