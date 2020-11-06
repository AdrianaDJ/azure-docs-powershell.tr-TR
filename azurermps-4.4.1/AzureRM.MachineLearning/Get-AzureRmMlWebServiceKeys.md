---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: 694ac928d78cf64f500730c57e394a8e3a425456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594651"
---
# Get-AzureRmMlWebServiceKeys

## SYNOPSIS
Web servisinin anahtarlarını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Bir Azure ML Web servisinin erişim tuşlarından birinin adı ve kaynak grubu.
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Verilen Web hizmeti örneğinin erişim kesy edinin.
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
Azure Machine Learning Web servisinin çalışma zamanı API 'Lerinin erişim tuşlarını alır.

## ÖRNEKLERDEN

### --------------------------Örnek 1-kaynak grubu ve adla belirtilen bir Web hizmeti için anahtarları alın--------------------------
@ {paragraf = PS C: \\ \> }





```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### --------------------------Örnek 2-Web hizmeti örneğinin anahtarlarını alın--------------------------
@ {paragraf = PS C: \\ \> }





```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

$mlService, Microsoft. Azure. Management. Machinöğrenim. WebServices. model. Webtürü türünde bir nesnedir.

## PARAMETRELERINE

### -MlWebService
Erişim tuşlarının alındığı Web hizmetinin adı.

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Get the access kesy for the given web service instance.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Erişim tuşlarının alındığı Web hizmetinin adı.

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Web hizmeti için kaynak grubu.

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
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

### Konumundaki
' MlWebService ' parametresi ardışık düzenin ' WebService ' türünün değerini kabul eder

## ÇıKıŞLAR

### Yabilirsiniz

## NOTLARıNDA
Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml

## ILGILI BAĞLANTıLAR

