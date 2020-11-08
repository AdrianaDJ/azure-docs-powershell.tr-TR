---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: eff689d36268f7eaec045c05c00d4fd18e91a026
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106973"
---
# Get-AzsDirectoryTenant

## SYNOPSIS
Geçerli aboneliğin ve verilen kaynak grubu adının altındaki tüm dizin kiracıları listeler.

## INDEKI

### Liste (varsayılan)
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### Al
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### Içermiyor
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## Tanım
Geçerli aboneliğin ve verilen kaynak grubu adının altındaki tüm dizin kiracıları listeler.

## ÖRNEKLERDEN

### --------------------------ÖRNEK 1--------------------------
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

Geçerli aboneliğin ve verilen kaynak grubu adının altındaki tüm dizin kiracıları listeler.

## PARAMETRELERINE

### -Ad
Dizin kiracı adı.

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
{{Fill ResourceGroupName açıklaması}}

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RESOURCEID
Kaynak kimliği.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Atla
Parametre değerinde belirtilen ilk N öğeyi atlayın.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -Üst
Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.
-Skip parametresinden sonra uygulanır.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. AzureStack. Management. abonelikler. admin. modeller. DirectoryTenant

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

