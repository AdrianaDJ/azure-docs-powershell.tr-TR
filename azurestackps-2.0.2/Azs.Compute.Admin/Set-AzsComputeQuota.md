---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/set-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 3229a6383d7159b31bf542add7374326d0de4ac4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106716"
---
# Set-AzsComputeQuota

## SYNOPSIS


## INDEKI

### Güncelleştir (varsayılan)
```
Set-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Güncelleştir (varsayılan)
```
Set-AzsComputeQuota -NewQuota <IQuota> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### Updategenişletilmiş
```
Set-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```
## Tanım
Işlem kotasını güncelleştirme

## ÖRNEKLERDEN

### Örnek 1: varolan bir hesaplama kotasındaki özellikleri ayarlama
```powershell
PS C:\> $myComputeQuota = Get-AzsComputeQuota -Name MyComputeQuota

PS C:\> $myComputeQuota.CoresLimit = 99; 

PS C:\> Set-AzsComputeQuota -NewQuota $myComputeQuota

AvailabilitySetCount               : 10
CoresLimit                         : 99
Id                                 : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/northwest/quotas/MyComputeQuota
Location                           : northwest
Name                               : MyComputeQuota
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

Komut satırında belirtilen parametreleri ayarlayın.
Ayarlanmamış tüm parametreler varsayılan olarak 0 değerini alır

## PARAMETRELERINE

### -DefaultProfile


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

### -NewQuota
Oluşturmak için, NEWQUOTA özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -SubscriptionID


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

### Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. Api20180209. ıquota

## ÇıKıŞLAR

### Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. Api20180209. ıquota



## NOTLARıNDA

KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun. Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.

YENIKOTA <IQuota> : 
  - `[Location <String>]`: Kaynağın konumu.
  - `[AvailabilitySetCount <Int32?>]`: İzin verilen en fazla kullanılabilirlik kümesi sayısı.
  - `[CoresLimit <Int32?>]`: İzin verilen maksimum çekirdek sayısı.
  - `[PremiumManagedDiskAndSnapshotSize <Int32?>]`: En fazla yönetilen disk sayısı ve Premium türü izin verilen anlık görüntü sayısı.
  - `[StandardManagedDiskAndSnapshotSize <Int32?>]`: En fazla yönetilen disk sayısı ve standart türü izin verilen anlık görüntü sayısı.
  - `[VMScaleSetCount <Int32?>]`: İzin verilen ölçek kümesi sayısı üst sınırı.
  - `[VirtualMachineCount <Int32?>]`: İzin verilen en fazla sanal makine sayısına izin verilir.

## ILGILI BAĞLANTıLAR

