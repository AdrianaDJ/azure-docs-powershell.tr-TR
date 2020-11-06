---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 58d15476921005b6da674d6a16441eb2e4f82865
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591200"
---
# Get-AzureRmAutomationDscOnboardingMetaconfig

## SYNOPSIS
Meta-Configuration. mof dosyaları oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Get-AzureRmAutomationDscOnboardingMetaconfig** cmdlet 'ı, APS Istenen durum yapılandırma (DSC) meta yapılandırma yönetilen nesne BIÇIMI (MOF) dosyalarını oluşturur.
Bu cmdlet, belirttiğiniz her bilgisayar adına bir. mof dosyası oluşturur.
Cmdlet. mof dosyaları için bir klasör oluşturur.
Bu bilgisayarlar için Set-DscLocalConfigurationManager cmdlet 'ini bir Azure Otomasyonu hesabında DSC düğümleri olarak eklemek için çalıştırabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: tüm sunucuları Automation DSC 'ye ekleme
```
PS C:\>Get-AzureRmAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

İlk komut, Contoso17 adlı Otomasyon hesabı için iki sunucu için DSC meta yapılandırma dosyaları oluşturur.
Komut bu dosyaları bir masaüstüne kaydeder.

İkinci komut, **set-DscLocalConfigurationManager** cmdlet 'ini kullanarak, meta yapılandırmasını DSC düğümleri olarak eklemek üzere belirtilen bilgisayarlara uygular.

## PARAMETRELERINE

### -AutomationAccountName
Otomasyon hesabının adını belirtir.
*ComputerName* parametresinin belirttiği bilgisayarları bu parametrenin belirttiği hesaba ekleyebilirsiniz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ComputerName
Bu cmdlet. MOF dosyalarını oluşturan bilgisayarların adları dizisini belirtir.
Bu parametreyi belirtmezseniz, cmdlet geçerli bilgisayar (localhost) için bir. mof dosyası oluşturur.

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

### -Force
Komutu onay istemeden çalışmaya zorlar ve aynı ada sahip mevcut. MOF dosyalarını değiştirebilirsiniz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFolder
Bu cmdlet. MOF dosyalarını depolayan bir klasörün adını belirtir.

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

### -ResourceGroupName
Kaynak grubunun adını belirtir.
Bu cmdlet, bu parametrenin belirttiği kaynak grubundaki bilgisayarlara. mof dosyaları oluşturur.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
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

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Automation. model. DscOnboardingMetaconfig

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

