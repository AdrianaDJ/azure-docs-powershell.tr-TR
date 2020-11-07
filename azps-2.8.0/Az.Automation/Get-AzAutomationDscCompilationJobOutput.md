---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
ms.openlocfilehash: 7a39d010759228e15dd5aee36788f9373ab879bb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753342"
---
# Get-AzAutomationDscCompilationJobOutput

## SYNOPSIS
Bir Automation DSC derleme işinin günlüğe kaydetme akışlarını alır.

## INDEKI

```
Get-AzAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azautomationdsccompilationjoi Input** cmdlet 'i, bir APS Istenen durum yapılandırma (DSC) derleme işinin akış kayıtlarını, Azure Otomasyonu 'nda alır.

## ÖRNEKLERDEN

### Örnek 1: DSC derleme işi için günlükleri alma
```
PS C:\>$Jobs = Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzAutomationDscCompilationJobOutput -Stream "Any"
```

İlk komut, Get-AzAutomationDscCompilationJob cmdlet 'ini kullanarak Contoso17 adlı Otomasyon hesabındaki derleme işlerini alır.
Komut bu nesneleri $Jobs değişkeninde depolar.
İkinci komut $Jobs dizisinin ilk üyesinin tüm akışı için derleme işi çıktısını alır.

## PARAMETRELERINE

### -AutomationAccountName
DSC derleme işini içeren Otomasyon hesabının adını belirtir.

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

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -ID
Bu cmdlet 'in çıkışı aldığı DSC derleme işinin benzersiz KIMLIĞINI belirtir.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in akış kayıtlarını aldığı DSC derleme işini içeren kaynak grubunun adını belirtir.

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

### -Başlangıçsaati
Başlangıç zamanını belirtir.
Bu cmdlet, DSC derleme işinin bu süreden sonra aldığı akış kayıtlarını alır.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Stream
Bu cmdlet 'in aldığı çıktı için akış türünü belirtir.
Geçerli değerler: 
- Tüm 
- Uyarılarla 
- Hatalar 
- Kapsamlı

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType
Parameter Sets: (All)
Aliases:
Accepted values: Warning, Error, Verbose, Any

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. Guid

### Microsoft. Azure. Commands. Automation. Common. CompilationJobStreamType

### System. Nullable ' 1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Automation. model. JobStream

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzAutomationDscCompilationJob](./Get-AzAutomationDscCompilationJob.md)

[Start-AzAutomationDscCompilationJob](./Start-AzAutomationDscCompilationJob.md)


