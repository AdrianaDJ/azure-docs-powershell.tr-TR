---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
ms.openlocfilehash: 4400cb375b60b4f961831927ed5763c608f8e5f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107997"
---
# New-AzApiManagementGroup

## SYNOPSIS
Bir API yönetim grubu oluşturur.

## INDEKI

```
New-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Yeni-Azapsananagementgroup** cmdlet 'ı bir API yönetim grubu oluşturur.

## ÖRNEKLERDEN

### Örnek 1: yönetim grubu oluşturma
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementGroup -Context $apimContext -Name "Group0001"
```

Bu komut bir yönetim grubu oluşturur.

### Örnek 2

Bir API yönetim grubu oluşturur. oluşturulmuş

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementGroup -Context <PsApiManagementContext> -Description 'Create Echo Api V4' -GroupId '0001' -Name 'Group0001' -Type Custom
```

## PARAMETRELERINE

### -Context
**Psapimanagementcontext** nesnesinin örneğini belirtir.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -Açıklama
Yönetim grubunun açıklamasını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ExternalID
Dış gruplar için bu özellik, dış kimlik sağlayıcısından grubun kimliğini içerir; örneğin, Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; Aksi takdirde değer null olur.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GroupID
Yeni yönetim grubunun tanımlayıcısını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Yönetim grubu adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tür
Grup türü. Özel grup Kullanıcı tanımlı gruptur. Sistem grubu yöneticiyi, geliştiricileri ve konukları içerir. Sistem grubu oluşturamaz veya güncelleştiremezsiniz.  Dış Grup, Azure Active Directory gibi dış kimlik sağlayıcısından gelen gruplarıdır. Bu parametre isteğe bağlıdır ve varsayılan olarak özel grup olarak kabul edilir.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType]
Parameter Sets: (All)
Aliases:
Accepted values: Custom, System, External

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext

### System. String

### System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananayöneti. ServiceManagement. modeller. Psapsananagementgrouptype, Microsoft. Azure. PowerShell. cmdlet

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgroup

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azapsananagementgroup](./Get-AzApiManagementGroup.md)

[Remove-Azapsananagementgroup](./Remove-AzApiManagementGroup.md)

[Set-Azapsananagementgroup](./Set-AzApiManagementGroup.md)


