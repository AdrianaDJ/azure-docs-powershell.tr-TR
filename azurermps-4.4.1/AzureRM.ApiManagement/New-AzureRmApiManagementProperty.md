---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
ms.openlocfilehash: cb50ea5735a9f63f5f35b8f1cb0648c566e6108d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764285"
---
# New-AzureRmApiManagementProperty

## SYNOPSIS
Yeni özellik oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tags <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**New-Azurermapsananagementproperty** cmdlet 'ı BIR Azure API Yönetim **özelliği** oluşturur.

## ÖRNEKLERDEN

### Örnek 1: etiketleri içeren özellik oluşturma
```
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

İlk komut $Tags değişkenine iki değer atar.

İkinci komut bir özellik oluşturur ve $Tags dizelere etiket olarak atar.

### Örnek 2: gizli değeri olan bir özellik oluşturma
```
PS C:\>New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

Bu komut şifrelenmiş bir değer içeren bir **özellik** oluşturur.

## PARAMETRELERINE

### -Context
**Psapsananagementcontext** nesnesini belirtir.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Bu cmdlet 'in oluşturduğu özelliğin adını belirtir.
Maksimum Uzunluk 100 karakterdir.
Adlar yalnızca harf, rakam, nokta, çizgi ve alt çizgi karakterlerini içerir.

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

### -PropertyId
Özelliğin KIMLIĞINI belirtir.
Maksimum uzunluk 256 karakterdir.
KIMLIK belirtmezseniz, bu cmdlet bir tane oluşturur.

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

### -Parola
Özellik değerinin gizli olduğunu ve şifrelenmesi gerektiğini belirtir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Etiketler
Bu cmdlet 'in özellikle ilişki kurduğu etiket dizisini belirtir.
Özellik listesini filtrelemek için Etiketler 'i kullanabilirsiniz.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Değer
Özellik için bir değer belirtir.
Bu değer ilke ifadeleri içerebilir.
Maksimum uzunluk 1000 karakterdir.
Değer boş olamaz veya yalnızca boşluklardan oluşamaz.

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

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproperty

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Remove-Azurermapsananagementproperty](./Remove-AzureRmApiManagementProperty.md)

[Set-Azurermapımanagementproperty](./Set-AzureRmApiManagementProperty.md)


