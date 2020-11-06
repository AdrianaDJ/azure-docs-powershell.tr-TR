---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 68ef1cf00adeec785faf3c3f43ff2e7dbcaafbc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594103"
---
# Get-AzureRmContainerRegistryCredential

## SYNOPSIS
Kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### NameResourceGroupParameterSet (varsayılan)
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RegistryObjectParameterSet
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Resourceıdparameterset
```
Get-AzureRmContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
Get-AzureRmContainerRegistryCredential cmdlet 'i kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini alır.

## ÖRNEKLERDEN

### Örnek 1: kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini alma
```powershell
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

Bu komut belirtilen kapsayıcı kayıt defterinin oturum açma kimlik bilgilerini alır.
Yönetici kullanıcısı, \` \` oturum açma kimlik bilgilerini almak amacıyla kapsayıcı kayıt defteri myregistry için etkinleştirilmelidir.

## PARAMETRELERINE

### -Ad
Kapsayıcı kayıt defteri adı.

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Registry
Kapsayıcısı.

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı.

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RESOURCEID
Kapsayıcı kayıt defteri kaynak kimliği

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### PSContainerRegistry
Parametre ' Registry ', ardışık düzenin ' PSContainerRegistry ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzureRmContainerRegistry](New-AzureRmContainerRegistry.md)

[Update-AzureRmContainerRegistry](Update-AzureRmContainerRegistry.md)

[Update-AzureRmContainerRegistryCredential](Update-AzureRmContainerRegistryCredential.md)

