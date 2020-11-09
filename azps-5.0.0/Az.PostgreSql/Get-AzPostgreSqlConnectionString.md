---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
ms.openlocfilehash: 8df35a38889e2c91bd74625ae916fd10739d9db1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325594"
---
# Get-AzPostgreSqlConnectionString

## SYNOPSIS
Bağlantı dizesini istemci bağlantı sağlayıcısına göre edinin.

## INDEKI

### Get (varsayılan)
```
Get-AzPostgreSqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Getviaıdentity
```
Get-AzPostgreSqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## Tanım
Bağlantı dizesini istemci bağlantı sağlayıcısına göre edinin.

## ÖRNEKLERDEN

### Örnek 1: kaynak grubuna ve sunucu adına göre PostgreSql Server bağlantı dizesini alma
```powershell
PS C:\> Get-AzPostgreSqlConnectionString -Client ADO.NET -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG

Server=postgresqltestserver.postgres.database.azure.com;Database={your_database};Port=5432;User Id=pwsh@postgresqltestserver;Password={your_password};Ssl Mode=Require;
```

Bu cmdlet, kaynak grubu ve sunucu adına göre PostgreSql Server bağlantı dizesini alır.

### Örnek 2: kimliğe göre PostgreSql Server bağlantı dizesini alma
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Get-AzPostgreSqlConnectionString -Client PHP

host=postgresqltestserver.postgres.database.azure.com port=5432 dbname={your_database} user=pwsh@postgresqltestserver password={your_password} sslmode=require
```

Bu cmdlet PostgreSql Server bağlantı dizesini kimlik ile alır.

## PARAMETRELERINE

### -İstemci
İstemci bağlantı sağlayıcısı.

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
Çoğaltmanın oluşturulacağı kaynak sunucu nesnesi.
Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Sunucunun adı.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

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
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionID
Bir Azure aboneliğini tanımlayan abonelik KIMLIĞI.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. Api20171201. IServer

## ÇıKıŞLAR

### System. String

## NOTLARıNDA

DIĞER adları

KARMAŞıK PARAMETRE ÖZELLIKLERI

Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun. Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.


INPUTOBJECT <IServer> : çoğaltmanın oluşturulacağı kaynak sunucu nesnesi.
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

