---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/set-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: c2cc0e7a22d7e581eece9004950b54bc0151fad3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106869"
---
# Set-AzsNetworkQuota

## SYNOPSIS
Kota oluşturun veya güncelleştirin.

## INDEKI

### Updategenişletilmiş (varsayılan)
```
Set-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Güncelleştiremedi
```
Set-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Tanım
Kota oluşturun veya güncelleştirin.

## ÖRNEKLERDEN

### --------------------------ÖRNEK 1--------------------------
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

Ağ kotasını ada göre güncelleştirin.

### --------------------------ÖRNEK 2--------------------------
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

Ağ kotasını ada göre güncelleştirin.

## PARAMETRELERINE

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

### -Konum
Kaynağın konumu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxLoadBalancersPerSubscription
Kiracı aboneliğinin hazırlayabileceğiniz maksimum yük dengeleyicili sayısı.

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxNicsPerSubscription
Kiracı aboneliğinin sağlaması için en fazla NIC sayısı.

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Maxpublicıpspersubscription
Kiracı aboneliğinin hazırlayabileceğiniz en fazla genel IP adresi sayısı.

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxSecurityGroupsPerSubscription
Kiracı aboneliğinin yapabileceği en fazla güvenlik grubu sayısı.

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxVirtualNetworkGatewayConnectionsPerSubscription
Kiracı aboneliğinin yapabileceği en fazla sanal ağ ağ geçidi bağlantısı sayısı.

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxVirtualNetworkGatewaysPerSubscription
Kiracı aboneliğinin hazırlayabileceğiniz sanal ağ geçidi sayısı üst sınırı.

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxVnetsPerSubscription
Kiracı aboneliğinin hazırlayabileceğiniz sanal ağ sayısı üst sınırı.

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Ad
Kaynağın adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Kota
Ağ kotası kaynağı.
Oluşturmak için, kota özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -SubscriptionID
Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.
Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### Etiketli
Anahtar değer çiftleri listesi.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
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

### Microsoft. Azure. PowerShell. cmdlet. NetworkAdmin. model. Api20150615. ıquota

## ÇıKıŞLAR

### Microsoft. Azure. PowerShell. cmdlet. NetworkAdmin. model. Api20150615. ıquota



## NOTLARıNDA

KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun. Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.

Kota <IQuota> : ağ kotası kaynağı.
  - `[Tag <IResourceTags>]`: Anahtar değer çiftleri listesi.
    - `[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.
  - `[MaxLoadBalancersPerSubscription <Int64?>]`: Kiracı aboneliğinin sağlaması için en fazla yük dengeleyicileri sayısı.
  - `[MaxNicsPerSubscription <Int64?>]`: Kiracı aboneliğinin sağlaması için en fazla NIC sayısı.
  - `[MaxPublicIpsPerSubscription <Int64?>]`: Kiracı aboneliğinin sağlaması için en fazla genel IP adresi sayısı.
  - `[MaxSecurityGroupsPerSubscription <Int64?>]`: Kiracı aboneliğinin sağlaması için en fazla güvenlik grubu sayısı.
  - `[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Kiracı aboneliğinin sağlaması için sanal ağ geçidi bağlantılarının en fazla sayısı.
  - `[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Kiracı aboneliğinin yapabileceği sanal ağ ağ geçidi sayısı üst sınırı.
  - `[MaxVnetsPerSubscription <Int64?>]`: Kiracı aboneliğinin yapabileceği sanal ağ sayısı üst sınırı.

## ILGILI BAĞLANTıLAR

