---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267404"
---
# Enable-AzContextAutosave

## SYNOPSIS
Azure bağlamları, komutları çalıştırmak için etkin aboneliğinizi ve bir Azure bulutuna bağlanmak için gereken kimlik doğrulama bilgilerini temsil eden PowerShell nesneleridir. Azure bağlamlarıyla, abonelikleri değiştirdiğinizde Azure PowerShell 'in hesabınızı yeniden doğrulaması gerekmez. Daha fazla bilgi [için bkz.](https://docs.microsoft.com/powershell/azure/context-persistence)

Bu cmdlet, bir PowerShell işlemini başlattığınızda Azure bağlam bilgilerinin kaydedilmesine ve otomatik olarak yüklenmesine olanak tanır. Örneğin, yeni bir pencere açarken.

## INDEKI

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım

Bir PowerShell süreci başlatıldığında Azure bağlam bilgilerinin kaydedilmesine ve otomatik olarak yüklenmesine olanak tanır. Bağlam, içeriği etkileyen tüm cmdlet yürütmesinin sonunda kaydedilir. Örneğin, herhangi bir profil cmdlet 'i. Kullanıcı kimlik doğrulamasını kullanıyorsanız, belirteçler çalıştırma sırasında belirteçler güncelleştirilebilir.

## ÖRNEKLERDEN

### Örnek 1: geçerli kullanıcı için otomatik kaydetme kimlik bilgilerini etkinleştirme

Geçerli Kullanıcı için kimlik bilgilerini otomatik kaydetme özelliğini açma. Bir PowerShell penceresi açıldığında, geçerli içeriğiniz oturum açmadan hatırlanır.

```powershell
Enable-AzContextAutosave
```

### Örnek 2

Bu PowerShell oturumunda, bir PowerShell penceresini açtığınızda Azure kimlik bilgileri, hesap ve abonelik bilgilerine izin verin ve otomatik olarak yüklenir. oluşturulmuş

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## PARAMETRELERINE

### -DefaultProfile

Azure ile iletişim için kullanılan kimlik bilgileri, kiracı ve abonelik

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

Bağlam değişikliklerinin kapsamını belirler. Örneğin, değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanıp uygulanmayacağı. Kapsamla yapılan değişiklikler, `CurrentUser` Kullanıcı tarafından başlatılan tüm PowerShell oturumlarını etkiler. Belirli bir oturumun farklı ayarları olması gerekiyorsa, kapsamı kullanın `Process` .

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: CurrentUser
Accept pipeline input: False
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Ortak Parametreler

Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
