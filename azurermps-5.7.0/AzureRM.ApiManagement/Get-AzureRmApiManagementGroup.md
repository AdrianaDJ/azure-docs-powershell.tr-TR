---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
ms.openlocfilehash: b77452bff93a9b66f8ffe54fdff623d391749622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592516"
---
# Get-AzureRmApiManagementGroup

## SYNOPSIS
Tüm veya belirli API Yönetim gruplarını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### GetAllGroups (varsayılan)
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Getbygroupıd
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Getbyuserıd
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Getbyproductıd
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azurermapımanagementgroup** cmdlet 'i veya belirli API Yönetim gruplarını alır.

## ÖRNEKLERDEN

### Örnek 1: tüm grupları Al
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext
```

Bu komut tüm grupları alır.

### Örnek 2: bir grup KIMLIĞI alma
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

Bu komut, 0123456789 adlı grup KIMLIĞINI alır.

### Örnek 3: ada göre grupla
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -Name "Group0002"
```

Bu komut, Group0002 adlı grubu alır.

### Örnek 4: tüm Kullanıcı gruplarını alma
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -UserId "0123456789"
```

Bu komut, 0123456789 adlı Kullanıcı KIMLIĞINE sahip tüm Kullanıcı gruplarını alır.

## PARAMETRELERINE

### -Context
Psapsananagementcontext örneğini belirtir.

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -GroupID
Grup KIMLIĞINI belirtir.
Belirtilmişse, cmdlet tanıtıcıyı tanımlayıcı tarafından bulmaya çalışır.

```yaml
Type: String
Parameter Sets: GetByGroupId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Yönetim grubunun adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ÜrünKimliği
Var olan ürünün tanıtıcısı.
Belirtilirse, ürünün atandığı tüm grupları döndürür.
Bu parametre isteğe bağlıdır.

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserID
Var olan ürünün tanımlayıcısını belirtir.
Belirtilmişse cmdlet, ürünün atandığı tüm grupları döndürür.

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgroup
API Yönetimi hizmeti 'nde yapılandırılan grubun ayrıntıları.

### IList<Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgroup>
API Yönetim hizmetinde yapılandırılmış grupların listesi.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-Azurermapımanagementgroup](./New-AzureRmApiManagementGroup.md)

[Remove-Azurermapımanagementgroup](./Remove-AzureRmApiManagementGroup.md)

[Set-Azurermapımanagementgroup](./Set-AzureRmApiManagementGroup.md)


