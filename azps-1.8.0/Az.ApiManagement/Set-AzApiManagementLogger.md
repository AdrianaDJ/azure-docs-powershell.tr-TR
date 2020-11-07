---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
ms.openlocfilehash: 4c7f4b4f308d04c6f9c82e70f9fbe0598bd4a9fb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917687"
---
# Set-AzApiManagementLogger

## SYNOPSIS
Bir API yönetim günlükçüsü değiştirir.

## INDEKI

### EventHubLoggerSet (varsayılan)
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Applicationınsightsloggerset
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-InstrumentationKey <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Set-Azapsananagementgünlükçü** cmdlet 'i, BIR Azure API Yönetim **günlükçüsü** ayarlarını değiştirir.

## ÖRNEKLERDEN

### Örnek 1: EventHub günlükçüsü değiştirme
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

Bu komut, KIMLIĞI Logger123 olan bir günlükçüsü değiştirir.

## PARAMETRELERINE

### -ConnectionString
İlke haklarını içeren bir Azure etkinliği hub bağlantı dizesini belirtir.

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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
Bir açıklama belirtir.

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

### -Enstrüentationkey
Application Insights 'ın alt yapısı. Bu parametre isteğe bağlıdır.

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Isarabellekli
Kayıt defterinde, yayımlamadan önce arabelleğe alınan kayıtların arabelleğe alınıp alınmayacağını belirtir.
Kayıtlar arabelleğe alındıklarında, her 15 saniyede bir olay hublara veya arabellek 256 KB ileti aldığında gönderilir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Loggerıd
Güncelleştirilecek günlükçü KIMLIĞINI belirtir.

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

### -Ad
Azure Classic Portal 'dan bir olay hub 'ının varlık adını belirtir.

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Geçiş
Bu cmdlet 'in değiştirdiği  **Psapsananagementgünlükçü** değerini geri aldığını gösterir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext

### System. String

### System. Management. Automation. SwitchParameter

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgünlükçü

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azapsananagementgünlükçü](./Get-AzApiManagementLogger.md)

[Yeni-Azsız](./New-AzApiManagementLogger.md)

[Remove-Azapsananagementgünlükçü](./Remove-AzApiManagementLogger.md)


