---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
ms.openlocfilehash: dcff41ecac3181da09ee2f1cf0673e4225c2802d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110046"
---
# Update-AzBlockchainTransactionNode

## SYNOPSIS
İşlem düğümünü güncelleyin.

## INDEKI

### Updategenişletilmiş (varsayılan)
```
Update-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Updateviaıdentitygenişletilmiş
```
Update-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Tanım
İşlem düğümünü güncelleyin.

## ÖRNEKLERDEN

### Örnek 1: bir transdüğümde güncelleştirme
```powershell
PS C:\> $tag = @{'key1'='update'}
PS C:\> Update-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode002 -ResourceGroupName testgroup -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

Bu komut, bir işlem düğümünü güncelleştirir.

### Örnek 2: bir transdüğüm düğümünü güncelleştirme
```powershell
PS C:\> $tag = @{'key2'='update'}
PS C:\> $tNode = Get-AzBlockchainMember -BlockchainMemberName dolauli002 -ResourceGroupName testgroup -Name transacnode002
PS C:\> Update-AzBlockchainTransactionNode -InputObject $tNode -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

Bu komut, bir işlem düğümünü güncelleştirir.

## PARAMETRELERINE

### -BlockchainMemberName
Blockzincir üye adı.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallRule
Güvenlik duvarı kurallarını alır veya ayarlar.
Oluşturmak için, FIREWALLRULE özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IFirewallRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
İşlem düğümü adı.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Parola
İşlem düğümü DNS uç noktası temel kimlik doğrulama parolasını ayarlar.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynağı içeren kaynak grubunun adı.
Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionID
Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.
Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. model. ıblockchainıdentity

## ÇıKıŞLAR

### Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. modeller. Api20180601Preview. ıctionnode

## NOTLARıNDA

DIĞER adları

KARMAŞıK PARAMETRE ÖZELLIKLERI

Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun. Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.


FIREWALLRULE <ıfirewallrule [] >: güvenlik duvarı kurallarını alır veya ayarlar.
  - `[EndIPAddress <String>]`: Güvenlik duvarı kuralı aralığının bitiş IP adresini alır veya ayarlar.
  - `[RuleName <String>]`: Güvenlik Duvarı kurallarının adını alır veya ayarlar.
  - `[StartIPAddress <String>]`: Güvenlik duvarı kuralı aralığının başlangıç IP adresini alır veya ayarlar.

INPUTOBJECT <IBlockchainIdentity> : IDENTITY parametresi
  - `[BlockchainMemberName <String>]`: Blockzincirine üye adı.
  - `[Id <String>]`: Kaynak kimliği yolu
  - `[Location <String>]`: Konum adı.
  - `[OperationId <String>]`: İşlem kimliği.
  - `[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı. Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.
  - `[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır. Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.
  - `[TransactionNodeName <String>]`: İşlem düğümü adı.

## ILGILI BAĞLANTıLAR

