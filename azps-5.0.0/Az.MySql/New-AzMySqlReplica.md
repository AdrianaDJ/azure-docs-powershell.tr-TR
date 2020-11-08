---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
ms.openlocfilehash: 5e5d83266dd86ccaf0bd5037c6af01f8b1846a69
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279391"
---
# New-AzMySqlReplica

## SYNOPSIS
Var olan veritabanından yeni bir çoğaltma oluşturur.

## INDEKI

```
New-AzMySqlReplica -Replica <String> -ResourceGroupName <String> -Master <IServer> [-SubscriptionId <String>]
 [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## Tanım
Var olan veritabanından yeni bir çoğaltma oluşturur.

## ÖRNEKLERDEN

### Örnek 1: yeni bir MySql Server çoğaltması oluşturma
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | New-AzMySqlReplica -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

Bu cmdlet yeni bir MySql sunucu yinelemesi oluşturur.

### Örnek 2: yeni bir MySql Server çoğaltması oluşturma
```powershell
PS C:\> $mysql = Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
PS C:\> New-AzMySqlReplica -Master $mysql -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

Parametre Yöneticisi (InputObject) ile bu cmdlet yeni bir MySql Server yinelemesi oluşturur.

## PARAMETRELERINE

### -Iş
Komutu iş olarak çalıştırır.

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
Kaynağın bulunduğu konum.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Master
Çoğaltmanın oluşturulacağı kaynak sunucu nesnesi.
Oluşturmak için, ana özellikler için Notlar bölümüne bakın ve karma tablo oluşturun.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NoWait
Komutu zaman uyumsuz olarak çalıştırır.

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

### -Çoğaltma
Sunucunun adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicaServerName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynağı içeren kaynak grubunun adı, bu değeri Azure Kaynak Yöneticisi API 'sinden veya portalınızdan edinebilirsiniz.

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

### -SKU
SKU 'nun adı, genellikle katman + aile + çekirdek; Örneğin, B_Gen4_1 GP_Gen5_8.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionID
Bir Azure aboneliğini tanımlayan abonelik KIMLIĞI.

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

### Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Api20171201. IServer

## ÇıKıŞLAR

### Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Api20171201. IServer

## NOTLARıNDA

DIĞER adları

KARMAŞıK PARAMETRE ÖZELLIKLERI

Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun. Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.


Ana <IServer> : çoğaltmanın oluşturulacağı kaynak sunucu nesnesi.
  - `Location <String>`: Kaynağın bulunduğu konum.
  - `[Tag <ITrackedResourceTags>]`: Anahtar-değer çiftleri biçiminde uygulamaya özgü meta veriler.
    - `[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.
  - `[AdministratorLogin <String>]`: Yöneticinin sunucunun oturum açma adı. Yalnızca sunucu oluşturulduğunda belirtilebilir (ve oluşturma için gereklidir).
  - `[EarliestRestoreDate <DateTime?>]`: En erken geri yükleme noktası oluşturulma zamanı (ISO8601 biçimi)
  - `[FullyQualifiedDomainName <String>]`: Sunucunun tam nitelikli etki alanı adı.
  - `[IdentityType <IdentityType?>]`: Kimlik türü. Kaynak için bir Azure Active Directory sorumlusu oluşturmak ve atamak için bunu ' SystemAssigned ' olarak ayarlayın.
  - `[InfrastructureEncryption <InfrastructureEncryption?>]`: Sunucunun altyapı şifrelemesinin etkin olup olmadığını gösteren durum.
  - `[MasterServerId <String>]`: Bir çoğaltma sunucusunun ana sunucu kimliği.
  - `[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Sunucunun en düşük TLS sürümünü zorunlu tutun.
  - `[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Bu sunucuda genel ağ erişimine izin verilip verilmeyeceğini. Değer isteğe bağlıdır, ancak geçirilirse ' Enabled ' veya ' Disabled ' olmalıdır
  - `[ReplicaCapacity <Int32?>]`: Ana sunucunun sahip olduğu en fazla yineleme sayısı.
  - `[ReplicationRole <String>]`: Sunucunun çoğaltma rolü.
  - `[SkuCapacity <Int32?>]`: Sunucunun COMPUTE birimlerini temsil eden ölçeklendirme/Out kapasitesi.
  - `[SkuFamily <String>]`: Donanım ailesi.
  - `[SkuName <String>]`: SKU 'nun adı, genellikle katman + aile + çekirdek; Örneğin, B_Gen4_1 GP_Gen5_8.
  - `[SkuSize <String>]`: Kaynak tarafından uygun şekilde yorumlanabilecek boyut kodu.
  - `[SkuTier <SkuTier?>]`: Belirli SKU 'nun katmanı, örneğin. temel.
  - `[SslEnforcement <SslEnforcementEnum?>]`: Sunucuya bağlanırken SSL zorlamayı etkinleştir veya yok.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: Sunucunun yedekleme bekletme günleri.
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: OneDrive 'ı etkinleştir-sunucu yedeklemesi için değil.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Otomatik büyüme özelliğini etkinleştir.
  - `[StorageProfileStorageMb <Int32?>]`: Sunucuda izin verilen maks depolama alanı.
  - `[UserVisibleState <ServerState?>]`: Kullanıcının görebileceği bir sunucunun durumu.
  - `[Version <ServerVersion?>]`: Sunucu sürümü.

## ILGILI BAĞLANTıLAR

