---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/new-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
ms.openlocfilehash: df6392e339063ccb2cc60411b77f73936071ab3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594944"
---
# New-AzureRmMlWebService

## SYNOPSIS
Yeni bir Web hizmeti oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### CreateFromFile
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Createfromınstance
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
Var olan bir kaynak grubunda bir Azure makine Learning Web hizmeti oluşturur.
Kaynak grubunda aynı ada sahip bir Web hizmeti varsa, çağrı bir güncelleştirme işlemi olarak çalışır ve mevcut Web servisinin üzerine yazılır.

## ÖRNEKLERDEN

### --------------------------Örnek 1: JSON dosyası temelinde yeni bir hizmet oluşturma--------------------------
```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

Başvurulan JSON dosyasındaki tanımlamayı temel alan "myresourcegroup" grubundaki "mywebservicename" adlı yeni bir Azure makine Learning Web hizmeti oluşturur.

### --------------------------Örnek 2: bir nesne örneğinden yeni bir hizmet oluşturun--------------------------
```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

Import-AzureRmMlWebService cmdlet 'ini kullanarak kaynak olarak yayımlamadan önce özelleştirmek için bir Web hizmeti nesnesi örneği edinebilirsiniz.

## PARAMETRELERINE

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

### -Definitionfıle
Web servisinin JSON Biçim tanımını içeren dosyanın yolunu içerir.
Web hizmeti tanımının en son belirtimini, altındaki Swagger belirtiminde bulabilirsiniz https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .

```yaml
Type: String
Parameter Sets: CreateFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Onay sorma.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Konum
Web hizmetinin bölgesi.
"Batı ABD" veya "Güneydoğu Asya" gibi bir Azure veri merkezi bölgesi girin.
Bu tür kaynakları destekleyen herhangi bir bölgeye Web hizmeti yerleştirebilirsiniz.
Web hizmetinin Azure aboneliğinizdeki aynı bölgede veya kaynak grubuyla aynı bölgede olması gerekmez.
Kaynak gruplarında farklı bölgelerden Web Hizmetleri bulunabilir.
Her kaynak türünü destekleyen bölgeleri belirlemek için, Get-AzureRmResourceProvider ProviderNamespace parametre cmdlet 'i ile kullanın.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Web hizmetinin adı.
Ad, kaynak grubunda benzersiz olmalıdır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewWebServiceDefinition
Hizmeti oluşturan tüm özellikleri içeren yeni Web hizmetinin tanımı.
Bu parametre gereklidir ve Microsoft. Azure. Management. Machinöğrenim. WebServices. model. WebService sınıfının bir örneğini temsil eder.
Web hizmeti tanımının en son belirtimini, altındaki Swagger belirtiminde bulabilirsiniz https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .

```yaml
Type: WebService
Parameter Sets: CreateFromInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Web servisinin yerleştirileceği kaynak grubu.
"Batı ABD" veya "Güneydoğu Asya" gibi bir Azure veri merkezi bölgesi girin.
Bu tür kaynakları destekleyen herhangi bir bölgeye Web hizmeti yerleştirebilirsiniz.
Web hizmetinin Azure aboneliğinizdeki aynı bölgede veya kaynak grubuyla aynı bölgede olması gerekmez.
Kaynak gruplarında farklı bölgelerden Web Hizmetleri bulunabilir.
Her kaynak türünü destekleyen bölgeleri belirlemek için, Get-AzureRmResourceProvider ProviderNamespace parametre cmdlet 'i ile kullanın.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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
' NewWebServiceDefinition ' parametresi ardışık düzenin ' WebService ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Azure. Management. machinöğrenim. WebServices. modeller. Web
Azure Machine Learning Web hizmetinin Özet açıklaması.
Var olan bir Web hizmetinde Get-AzureRmMlWebService cmdlet 'i çağırarak döndürülen açıklamaya benzer.
Bu açıklama, depolama hesabının kimlik bilgileri ve hizmetin erişim tuşları gibi hassas özellikler içermez.

## NOTLARıNDA
Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml

## ILGILI BAĞLANTıLAR

