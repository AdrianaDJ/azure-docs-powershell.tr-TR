---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: 555409187d2d48476a731be344d0404efddc946c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935259"
---
# Get-AzContextAutosaveSetting

## SYNOPSIS
İçeriğin otomatik olarak kaydedilip kaydedilmeyeceği ve kaydedilen içeriğin ve kimlik bilgilerinin bulunabileceği yerlerde, bağlam otomatik kaydetme özelliğiyle ilgili meta verileri görüntüler.

## INDEKI

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
İçeriğin otomatik olarak kaydedilip kaydedilmeyeceği ve kaydedilen içeriğin ve kimlik bilgilerinin bulunabileceği yerlerde, bağlam otomatik kaydetme özelliğiyle ilgili meta verileri görüntüler.

## ÖRNEKLERDEN

### Geçerli oturumda bağlam kaydetme meta verilerini alma
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

İçeriğin kaydedilip kaydedilmeyeceği hakkında ayrıntılı bilgi edinin.  Yukarıdaki örnekte, otomatik kaydetme özelliği devre dışı bırakılmıştır.

### Geçerli Kullanıcı için bağlam kaydetme meta verilerini alma
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

İçeriğin geçerli kullanıcı için varsayılan olarak kaydedilip kaydedilmeyeceği hakkında ayrıntılı bilgi edinin.  Bu, geçerli oturumda etkin olan ayarlardan farklı olabilir. Yukarıdaki örnekte, Otomatik Kaydet özelliği etkinleştirilmiştir ve veriler varsayılan konuma kaydedilir.

## PARAMETRELERINE

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

### -Kapsam
Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
