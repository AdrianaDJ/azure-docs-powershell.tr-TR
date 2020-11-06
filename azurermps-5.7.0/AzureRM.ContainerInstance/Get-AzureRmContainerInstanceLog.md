---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/get-azurermcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
ms.openlocfilehash: 346973683ca7e360c4b4d63a4f2ed4f4856a0797
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586751"
---
# Get-AzureRmContainerInstanceLog

## SYNOPSIS
Kapsayıcı grubundaki bir kapsayıcı örneğinin günlüklerini alın.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Getcontainerınstancelogbynamesparamset (varsayılan)
```
Get-AzureRmContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Getcontainerınstancelogbypscontainergroupparamset
```
Get-AzureRmContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Getcontainerınstancelogbyresourceıdparamset
```
Get-AzureRmContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmContainerInstanceLog** cmdlet 'i, kapsayıcı grubundaki bir kapsayıcının günlüklerini alır.

## ÖRNEKLERDEN

### Örnek 1: kapsayıcı örneğinin kuyruk günlüğünü alma
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

`container1`Kapsayıcıyı kapsayıcı grubunda alın `mycontainer` . Varsayılan olarak, en fazla 4MB günlük içeriği döndürür.

### Örnek 2: kapsayıcı grubuyla aynı ada sahip bir kapsayıcı örneğinin kuyruk günlüğünü alma
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

`mycontainer`Kapsayıcıyı kapsayıcı grubunda alın `mycontainer` . Varsayılan olarak, en fazla 4MB günlük içeriği döndürür.

### Örnek 3: kapsayıcı örneğinin günlük dizi 2 satırlarını alma
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

Konteyner grubunda günlüğün 2 satır sonu alın `container1` `mycontainer` .

### Örnek 4: kapsayıcı grubunda bir kapsayıcı örneğinin kuyruk günlüğünü
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzureRmContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

Konteyner grubunda oturum açma bölümünden oturum açın `mycontainer` `mycontainer` . Varsayılan olarak, en fazla 4MB günlük içeriği döndürür.

## PARAMETRELERINE

### -ContainerGroupName
Kapsayıcı grubu adı.

```yaml
Type: String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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

### -Inputcontainergroup
Giriş kapsayıcısı Grup nesnesi.

```yaml
Type: PSContainerGroup
Parameter Sets: GetContainerInstanceLogByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Kapsayıcı grubundaki kapsayıcı örneği adı.
Varsayılan: kapsayıcı grubu adıyla aynıdır

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

### -ResourceGroupName
Kaynak grubu adı.

```yaml
Type: String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RESOURCEID
Kaynak kimliği.

```yaml
Type: String
Parameter Sets: GetContainerInstanceLogByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Kuyruklu
Günlükte kuyruk uygulanacak satır sayısı.
Belirtistemezseniz, cmdlet, 4MB kuyruklu günlük

```yaml
Type: Int32
Parameter Sets: (All)
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

### Microsoft. Azure. Commands. Containerınstance. modeller. PSContainerGroup

## ÇıKıŞLAR

### System. String

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
