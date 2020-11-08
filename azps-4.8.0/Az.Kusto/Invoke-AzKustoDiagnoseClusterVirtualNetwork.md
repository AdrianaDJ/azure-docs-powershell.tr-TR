---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodiagnoseclustervirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
ms.openlocfilehash: 682de416a4aba61e1f287661c88faee9e20d248c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273552"
---
# Invoke-AzKustoDiagnoseClusterVirtualNetwork

## SYNOPSIS
Hizmetin bağımlı olduğu dış kaynaklar için ağ bağlantısı durumunu tanılar.

## INDEKI

### Tanıla (varsayılan)
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### DiagnoseViaIdentity
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Tanım
Hizmetin bağımlı olduğu dış kaynaklar için ağ bağlantısı durumunu tanılar.

## ÖRNEKLERDEN

### Örnek 1: dış kaynaklar için ağ bağlantısı tanılaması 'nı göster 
```powershell
PS C:\> Invoke-AzKustoDiagnoseClusterVirtualNetwork -ResourceGroupName "testrg" -ClusterName "testnewkustocluster"

```

Yukarıdaki komut, "testnewkustocluster" kümesinin bağlı olduğu dış kaynaklar için ağ bağlantısı durumunu tanılar

## PARAMETRELERINE

### -Iş
Komutu iş olarak çalıştırmak

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClusterName
Kusto kümesinin adı.

```yaml
Type: System.String
Parameter Sets: Diagnose
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

### -InputObject
Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DiagnoseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NoWait
Komutu zaman uyumsuz olarak çalıştırır

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kusto kümesini içeren kaynak grubunun adı.

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionID
Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.
Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.

```yaml
Type: System.String
Parameter Sets: Diagnose
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

### Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity

## ÇıKıŞLAR

### System. String

## NOTLARıNDA

DIĞER adları

KARMAŞıK PARAMETRE ÖZELLIKLERI

Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun. Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.


INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi
  - `[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.
  - `[ClusterName <String>]`: Kusto kümesinin adı.
  - `[DataConnectionName <String>]`: Veri bağlantısının adı.
  - `[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.
  - `[Id <String>]`: Kaynak kimliği yolu
  - `[Location <String>]`: Azure konumu.
  - `[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.
  - `[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.
  - `[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.

## ILGILI BAĞLANTıLAR

