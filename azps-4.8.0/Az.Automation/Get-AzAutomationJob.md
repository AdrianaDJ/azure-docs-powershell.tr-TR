---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: 31390ccb19574b6b88c26828bf504dbc8ac5d924
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107959"
---
# Get-AzAutomationJob

## SYNOPSIS
Otomasyon Runbook işlerini alır.

## INDEKI

### Tümü (varsayılan)
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Byjobıd
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRunbookName
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzAutomationJob** cmdlet 'ı, Azure Otomasyonu 'ndaki runbook işlerini alır.

## ÖRNEKLERDEN

### Örnek 1: belirli bir runbook işini edinme
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

Bu komut belirtilen GUID 'ye sahip işi alır.

### Örnek 2: runbook için tüm işleri alma
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

Bu komut, Runbook02 adındaki runbook ile ilişkili tüm işleri alır.

### Örnek 3: çalışan tüm işleri alma
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

Bu komut, Contoso17 adlı Otomasyon hesabında çalışan tüm işleri alır.

## PARAMETRELERINE

### -AutomationAccountName
Bu cmdlet 'in işleri aldığı Otomasyon hesabının adını belirtir.

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

### -Bitişsaati
Bir işin bitiş zamanını **DateTimeOffset** nesnesi olarak belirtir.
Geçerli bir **DateTimeOffset** 'e dönüştürülebilecek bir dize belirtebilirsiniz.
Bu cmdlet, bitiş saati olan işleri bu parametrenin belirttiği değerle alır.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Bu cmdlet 'in aldığı bir işin KIMLIĞINI belirtir.

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in işleri aldığı kaynak grubunun adını belirtir.

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

### -RunbookName
Bu cmdlet 'in işleri aldığı runbook 'un adını belirtir.

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Başlangıçsaati
Bir işin başlangıç saatini **DateTimeOffset** nesnesi olarak belirtir.
Bu cmdlet, başlangıç saati olan veya bu parametrenin belirttiği değerden sonraki işleri alır.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Durum
İşin durumunu belirtir.
Bu cmdlet, Bu parametreyle eşleşen bir durumu olan işleri alır.
Geçerli değerler: 
- Etkinleştirirken
- Tamamladığı
- Erişilemedi
- Sıradan
- İlirken
- Çalışması
- Başlarken
- Sahiptir
- Arak
- Etsin
- Et

```yaml
Type: System.String
Parameter Sets: ByAll, ByRunbookName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. Guid

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Automation. model. job

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azautomationjoi koyma](./Get-AzAutomationJobOutput.md)

[Özgeçmiş-AzAutomationJob](./Resume-AzAutomationJob.md)

[Stop-AzAutomationJob](./Stop-AzAutomationJob.md)

[Askıya alma-AzAutomationJob](./Suspend-AzAutomationJob.md)


