---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: 7bece0fd2a9de822a5fa2a513fc06d4d20d96e4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279116"
---
# Get-AzAutomationJobOutputRecord

## SYNOPSIS
Bir Otomasyon iş çıkışı kaydının tam çıkışını alır.

## INDEKI

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azautomationjoi Putrecord** cmdlet 'i, bir otomatikleştirme iş çıkışı kaydının tam çıkışını alır.
**Get-Azautomationjoverınput** cmdlet 'inin bir veya daha fazla iş çıkışı kaydını listemesine rağmen, herhangi bir çıktı kaydının değerinin yalnızca bir özetini döndürür.
Bir çıkış kaydının çıkış değerinin başlangıç türü olarak tam değerini döndürmez.
Ayrıca özetin, bu cmdlet 'in çıktısı olan tam değerin aşılabildiği en büyük uzunluğu vardır.

## ÖRNEKLERDEN

### Örnek 1: Otomasyon işinin tam çıkışını alma
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

Bu komut, işin belirtilen iş KIMLIĞINE sahip tam çıkışını alır.

## PARAMETRELERINE

### -AutomationAccountName
Bu cmdlet 'in iş çıkışı kaydını aldığı Otomasyon hesabının adını belirtir.

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
Bu cmdlet 'in alınacağı iş çıkışı kaydının KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobId
Bu cmdlet 'in çıkış kaydı aldığı iş KIMLIĞINI belirtir.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in iş çıkışı kaydını aldığı kaynak grubunun adını belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. Guid

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Automation. model. JobStreamRecord

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azautomationjoi koyma](./Get-AzAutomationJobOutput.md)


