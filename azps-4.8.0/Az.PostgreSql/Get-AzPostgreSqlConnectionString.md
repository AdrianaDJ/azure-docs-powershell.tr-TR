---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
ms.openlocfilehash: 8df35a38889e2c91bd74625ae916fd10739d9db1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108784"
---
# <span data-ttu-id="a30ee-101">Get-AzPostgreSqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="a30ee-101">Get-AzPostgreSqlConnectionString</span></span>

## <span data-ttu-id="a30ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a30ee-102">SYNOPSIS</span></span>
<span data-ttu-id="a30ee-103">Bağlantı dizesini istemci bağlantı sağlayıcısına göre edinin.</span><span class="sxs-lookup"><span data-stu-id="a30ee-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="a30ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a30ee-104">SYNTAX</span></span>

### <span data-ttu-id="a30ee-105">Get (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a30ee-105">Get (Default)</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a30ee-106">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="a30ee-106">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a30ee-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a30ee-107">DESCRIPTION</span></span>
<span data-ttu-id="a30ee-108">Bağlantı dizesini istemci bağlantı sağlayıcısına göre edinin.</span><span class="sxs-lookup"><span data-stu-id="a30ee-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="a30ee-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a30ee-109">EXAMPLES</span></span>

### <span data-ttu-id="a30ee-110">Örnek 1: kaynak grubuna ve sunucu adına göre PostgreSql Server bağlantı dizesini alma</span><span class="sxs-lookup"><span data-stu-id="a30ee-110">Example 1: Get PostgreSql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConnectionString -Client ADO.NET -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG

Server=postgresqltestserver.postgres.database.azure.com;Database={your_database};Port=5432;User Id=pwsh@postgresqltestserver;Password={your_password};Ssl Mode=Require;
```

<span data-ttu-id="a30ee-111">Bu cmdlet, kaynak grubu ve sunucu adına göre PostgreSql Server bağlantı dizesini alır.</span><span class="sxs-lookup"><span data-stu-id="a30ee-111">This cmdlet gets PostgreSql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="a30ee-112">Örnek 2: kimliğe göre PostgreSql Server bağlantı dizesini alma</span><span class="sxs-lookup"><span data-stu-id="a30ee-112">Example 2: Get PostgreSql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Get-AzPostgreSqlConnectionString -Client PHP

host=postgresqltestserver.postgres.database.azure.com port=5432 dbname={your_database} user=pwsh@postgresqltestserver password={your_password} sslmode=require
```

<span data-ttu-id="a30ee-113">Bu cmdlet PostgreSql Server bağlantı dizesini kimlik ile alır.</span><span class="sxs-lookup"><span data-stu-id="a30ee-113">This cmdlet gets PostgreSql server connection string by identity.</span></span>

## <span data-ttu-id="a30ee-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a30ee-114">PARAMETERS</span></span>

### <span data-ttu-id="a30ee-115">-İstemci</span><span class="sxs-lookup"><span data-stu-id="a30ee-115">-Client</span></span>
<span data-ttu-id="a30ee-116">İstemci bağlantı sağlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="a30ee-116">Client connection provider.</span></span>

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

### <span data-ttu-id="a30ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a30ee-117">-DefaultProfile</span></span>
<span data-ttu-id="a30ee-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a30ee-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a30ee-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a30ee-119">-InputObject</span></span>
<span data-ttu-id="a30ee-120">Çoğaltmanın oluşturulacağı kaynak sunucu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a30ee-120">The source server object to create replica from.</span></span>
<span data-ttu-id="a30ee-121">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a30ee-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a30ee-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="a30ee-122">-Name</span></span>
<span data-ttu-id="a30ee-123">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="a30ee-123">The name of the server.</span></span>

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

### <span data-ttu-id="a30ee-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a30ee-124">-ResourceGroupName</span></span>
<span data-ttu-id="a30ee-125">Kaynağı içeren kaynak grubunun adı, bu değeri Azure Kaynak Yöneticisi API 'sinden veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a30ee-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a30ee-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a30ee-126">-SubscriptionId</span></span>
<span data-ttu-id="a30ee-127">Bir Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a30ee-127">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="a30ee-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a30ee-128">CommonParameters</span></span>
<span data-ttu-id="a30ee-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a30ee-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a30ee-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a30ee-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a30ee-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a30ee-131">INPUTS</span></span>

### <span data-ttu-id="a30ee-132">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="a30ee-132">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="a30ee-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a30ee-133">OUTPUTS</span></span>

### <span data-ttu-id="a30ee-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a30ee-134">System.String</span></span>

## <span data-ttu-id="a30ee-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a30ee-135">NOTES</span></span>

<span data-ttu-id="a30ee-136">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="a30ee-136">ALIASES</span></span>

<span data-ttu-id="a30ee-137">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="a30ee-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a30ee-138">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a30ee-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a30ee-139">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a30ee-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a30ee-140">INPUTOBJECT <IServer> : çoğaltmanın oluşturulacağı kaynak sunucu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a30ee-140">INPUTOBJECT <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="a30ee-141">`Location <String>`: Kaynağın bulunduğu konum.</span><span class="sxs-lookup"><span data-stu-id="a30ee-141">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="a30ee-142">`[Tag <ITrackedResourceTags>]`: Anahtar-değer çiftleri biçiminde uygulamaya özgü meta veriler.</span><span class="sxs-lookup"><span data-stu-id="a30ee-142">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="a30ee-143">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a30ee-143">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a30ee-144">`[AdministratorLogin <String>]`: Yöneticinin sunucunun oturum açma adı.</span><span class="sxs-lookup"><span data-stu-id="a30ee-144">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="a30ee-145">Yalnızca sunucu oluşturulduğunda belirtilebilir (ve oluşturma için gereklidir).</span><span class="sxs-lookup"><span data-stu-id="a30ee-145">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="a30ee-146">`[EarliestRestoreDate <DateTime?>]`: En erken geri yükleme noktası oluşturulma zamanı (ISO8601 biçimi)</span><span class="sxs-lookup"><span data-stu-id="a30ee-146">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="a30ee-147">`[FullyQualifiedDomainName <String>]`: Sunucunun tam nitelikli etki alanı adı.</span><span class="sxs-lookup"><span data-stu-id="a30ee-147">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="a30ee-148">`[IdentityType <IdentityType?>]`: Kimlik türü.</span><span class="sxs-lookup"><span data-stu-id="a30ee-148">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="a30ee-149">Kaynak için bir Azure Active Directory sorumlusu oluşturmak ve atamak için bunu ' SystemAssigned ' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a30ee-149">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="a30ee-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Sunucunun altyapı şifrelemesinin etkin olup olmadığını gösteren durum.</span><span class="sxs-lookup"><span data-stu-id="a30ee-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="a30ee-151">`[MasterServerId <String>]`: Bir çoğaltma sunucusunun ana sunucu kimliği.</span><span class="sxs-lookup"><span data-stu-id="a30ee-151">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="a30ee-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Sunucunun en düşük TLS sürümünü zorunlu tutun.</span><span class="sxs-lookup"><span data-stu-id="a30ee-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="a30ee-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Bu sunucuda genel ağ erişimine izin verilip verilmeyeceğini.</span><span class="sxs-lookup"><span data-stu-id="a30ee-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="a30ee-154">Değer isteğe bağlıdır, ancak geçirilirse ' Enabled ' veya ' Disabled ' olmalıdır</span><span class="sxs-lookup"><span data-stu-id="a30ee-154">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="a30ee-155">`[ReplicaCapacity <Int32?>]`: Ana sunucunun sahip olduğu en fazla yineleme sayısı.</span><span class="sxs-lookup"><span data-stu-id="a30ee-155">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="a30ee-156">`[ReplicationRole <String>]`: Sunucunun çoğaltma rolü.</span><span class="sxs-lookup"><span data-stu-id="a30ee-156">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="a30ee-157">`[SkuCapacity <Int32?>]`: Sunucunun COMPUTE birimlerini temsil eden ölçeklendirme/Out kapasitesi.</span><span class="sxs-lookup"><span data-stu-id="a30ee-157">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="a30ee-158">`[SkuFamily <String>]`: Donanım ailesi.</span><span class="sxs-lookup"><span data-stu-id="a30ee-158">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="a30ee-159">`[SkuName <String>]`: SKU 'nun adı, genellikle katman + aile + çekirdek; Örneğin, B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="a30ee-159">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="a30ee-160">`[SkuSize <String>]`: Kaynak tarafından uygun şekilde yorumlanabilecek boyut kodu.</span><span class="sxs-lookup"><span data-stu-id="a30ee-160">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="a30ee-161">`[SkuTier <SkuTier?>]`: Belirli SKU 'nun katmanı, örneğin. temel.</span><span class="sxs-lookup"><span data-stu-id="a30ee-161">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="a30ee-162">`[SslEnforcement <SslEnforcementEnum?>]`: Sunucuya bağlanırken SSL zorlamayı etkinleştir veya yok.</span><span class="sxs-lookup"><span data-stu-id="a30ee-162">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="a30ee-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Sunucunun yedekleme bekletme günleri.</span><span class="sxs-lookup"><span data-stu-id="a30ee-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="a30ee-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: OneDrive 'ı etkinleştir-sunucu yedeklemesi için değil.</span><span class="sxs-lookup"><span data-stu-id="a30ee-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="a30ee-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Otomatik büyüme özelliğini etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="a30ee-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="a30ee-166">`[StorageProfileStorageMb <Int32?>]`: Sunucuda izin verilen maks depolama alanı.</span><span class="sxs-lookup"><span data-stu-id="a30ee-166">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="a30ee-167">`[UserVisibleState <ServerState?>]`: Kullanıcının görebileceği bir sunucunun durumu.</span><span class="sxs-lookup"><span data-stu-id="a30ee-167">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="a30ee-168">`[Version <ServerVersion?>]`: Sunucu sürümü.</span><span class="sxs-lookup"><span data-stu-id="a30ee-168">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="a30ee-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a30ee-169">RELATED LINKS</span></span>

