---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: c747d85f87e88c3f72ae86c8bcef771b3e42c91a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587328"
---
# Set-AzureRmApiManagementSubscription

## SYNOPSIS
Var olan abonelik ayrıntılarını ayarlar.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Set-Azurermapsananagementsubscription** cmdlet 'i var olan abonelik ayrıntılarını ayarlar.

## ÖRNEKLERDEN

### Örnek 1: aboneliğin durumunu ve birincil ve ikincil anahtarlarını ayarlama
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

Bu komut abonelik için birincil ve ikincil anahtarları ayarlar ve etkinleştirir.

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

### -ExpiresOn
Abonelik son kullanım tarihini belirtir.
Bu parametrenin varsayılan değeri $Null.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Abonelik adını belirtir.

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

### -Geçiş
geçiş

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

### -PrimaryKey
Abonelik birincil anahtarını belirtir.
Bu parametre belirtilmemişse otomatik olarak oluşturulur.
Bu parametre 1-300 karakter uzunluğunda olmalıdır.

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

### -Secondaryanahtarı
Abonelik ikincil anahtarını belirtir.
Bu parametre belirtilmemişse otomatik olarak oluşturulur.
Bu parametre 1-300 karakter uzunluğunda olmalıdır.

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

### Durumlu
Abonelik durumunu belirtir.
Bu parametrenin varsayılan değeri $Null.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState]
Parameter Sets: (All)
Aliases:
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StateComment
Abonelik durumu açıklamasını belirtir.
Bu parametrenin varsayılan değeri $Null.

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

### -SubscriptionID
Abonelik KIMLIĞINI belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext

### System. String

### System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. PsApiManagementSubscriptionState, Microsoft. Azure. Commands

### System. Nullable ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

### System. Management. Automation. SwitchParameter

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscription

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermapımanagementsubscription](./Get-AzureRmApiManagementSubscription.md)

[Yeni-Azurermapımanagementsubscription](./New-AzureRmApiManagementSubscription.md)

[Remove-Azurermapımanagementsubscription](./Remove-AzureRmApiManagementSubscription.md)


