---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 732c7cd1feb54c1475839a39f57f81d154da80ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586682"
---
# Set-AzureRmIntegrationAccountGeneratedIcn

## SYNOPSIS
Azure Kaynak grubundaki tümleştirme hesabı tarafından oluşturulan değişim denetim numarasını (ıCN) güncelleştirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Tanım
Set-AzureRmIntegrationAccountGeneratedIcn cmdlet 'i, mevcut bir tümleştirme hesabını güncelleştirir değişim denetim numarası (ıCN)
Bu cmdlet 'i, tümleştirme hesabı oluşturulmuş değişim denetim numarasını güncelleştirmek için kullanın.
Tümleştirme hesabı adını, kaynak grubu adını ve anlaşma adını belirterek, tümleştirme hesabı tarafından oluşturulan bir değişim denetim numarasını güncelleyebilirsiniz.
Bu komutla yeni bir tümleştirme hesabı oluşturma
Dinamik parametreleri kullanmak için, bunları komuta yazın veya parametre adını belirtmek için bir kısa çizgi işareti (-) yazın ve ardından kullanılabilir parametreler arasında ilerlemek için SEKME tuşuna art arda basın.
Gerekli bir şablon parametresini kaçırırsanız cmdlet, sizden değer ister.
Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.
Lütfen x12 veya Ediolgu denetim numaralarının döndürülmesini isteyip istemediğinizi belirtmek için "-AgreementType" parametresini sağlayın

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "X12IntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType X12 -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

Bu komut, belirli bir tümleştirme hesabı anlaşması için x12 Interchange Control numarası üretilen tümleştirme hesabını alır, değerini 100 ile artırıp güncelleştirilmiş değeri yeniden yazar.

### Örnek 2
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "EdifactIntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType EdifactIntegrationAccountAgreement -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

Bu komut, belirli bir tümleştirme hesabı anlaşması için Edıfactıntegrationaccountagreement Interchange için Integration hesabını alır, değerini 100 ile artırıp güncelleştirilmiş değeri geri yazar.

## PARAMETRELERINE

### -AgreementName
Tümleştirme hesabı anlaşma adı.

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

### -AgreementType
Tümleştirme hesabı anlaşma türü.

```yaml
Type: String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ControlNumber
Oluşturulan denetim numarası yeni değer.

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

### -Ad
Tümleştirme hesabı adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Tümleştirme hesabı kaynak grubu adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Logicuyg. Utilities. ıntegrationaccountclient + ıntegrationaccountcontrolnumber

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmIntegrationAccountGeneratedIcn](./Get-AzureRmIntegrationAccountGeneratedIcn.md)

