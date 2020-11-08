---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
ms.openlocfilehash: e3c0d7e8d3b3d9fe42bc97c40ad54424b7bfd0da
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265831"
---
# <span data-ttu-id="aac7f-101">New-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="aac7f-101">New-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="aac7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aac7f-102">SYNOPSIS</span></span>
<span data-ttu-id="aac7f-103">Var olan veritabanından yeni bir çoğaltma oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aac7f-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="aac7f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aac7f-104">SYNTAX</span></span>

```
New-AzPostgreSqlReplica -ReplicaName <String> -ResourceGroupName <String> -Master <IServer>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aac7f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aac7f-105">DESCRIPTION</span></span>
<span data-ttu-id="aac7f-106">Var olan veritabanından yeni bir çoğaltma oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aac7f-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="aac7f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aac7f-107">EXAMPLES</span></span>

### <span data-ttu-id="aac7f-108">Örnek 1: yeni bir PostgreSql Server çoğaltması oluşturma</span><span class="sxs-lookup"><span data-stu-id="aac7f-108">Example 1: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | New-AzPostgreSqlReplica -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="aac7f-109">Bu cmdlet yeni bir PostgreSql sunucu yinelemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aac7f-109">This cmdlet creates a new PostgreSql server replica.</span></span>

### <span data-ttu-id="aac7f-110">Örnek 2: yeni bir PostgreSql Server çoğaltması oluşturma</span><span class="sxs-lookup"><span data-stu-id="aac7f-110">Example 2: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> $pgDb = Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 
PS C:\> New-AzPostgreSqlReplica -Master $pgDb -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="aac7f-111">Bu cmdlet yeni bir PostgreSql sunucu yinelemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aac7f-111">This cmdlet creates a new PostgreSql server replica.</span></span>

## <span data-ttu-id="aac7f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aac7f-112">PARAMETERS</span></span>

### <span data-ttu-id="aac7f-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="aac7f-113">-AsJob</span></span>
<span data-ttu-id="aac7f-114">Komutu iş olarak çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="aac7f-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="aac7f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aac7f-115">-DefaultProfile</span></span>
<span data-ttu-id="aac7f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aac7f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aac7f-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="aac7f-117">-Location</span></span>
<span data-ttu-id="aac7f-118">Kaynağın bulunduğu konum.</span><span class="sxs-lookup"><span data-stu-id="aac7f-118">The location the resource resides in.</span></span>

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

### <span data-ttu-id="aac7f-119">-Master</span><span class="sxs-lookup"><span data-stu-id="aac7f-119">-Master</span></span>
<span data-ttu-id="aac7f-120">Çoğaltmanın oluşturulacağı kaynak sunucu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="aac7f-120">The source server object to create replica from.</span></span>
<span data-ttu-id="aac7f-121">Oluşturmak için, ana özellikler için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="aac7f-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aac7f-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="aac7f-122">-NoWait</span></span>
<span data-ttu-id="aac7f-123">Komutu zaman uyumsuz olarak çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="aac7f-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="aac7f-124">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="aac7f-124">-ReplicaName</span></span>
<span data-ttu-id="aac7f-125">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="aac7f-125">The name of the server.</span></span>

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

### <span data-ttu-id="aac7f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aac7f-126">-ResourceGroupName</span></span>
<span data-ttu-id="aac7f-127">Kaynağı içeren kaynak grubunun adı, bu değeri Azure Kaynak Yöneticisi API 'sinden veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aac7f-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="aac7f-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="aac7f-128">-Sku</span></span>
<span data-ttu-id="aac7f-129">SKU 'nun adı, genellikle katman + aile + çekirdek; Örneğin, B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="aac7f-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="aac7f-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="aac7f-130">-SubscriptionId</span></span>
<span data-ttu-id="aac7f-131">Bir Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="aac7f-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="aac7f-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="aac7f-132">-Confirm</span></span>
<span data-ttu-id="aac7f-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aac7f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aac7f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aac7f-134">-WhatIf</span></span>
<span data-ttu-id="aac7f-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aac7f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aac7f-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aac7f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aac7f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac7f-137">CommonParameters</span></span>
<span data-ttu-id="aac7f-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aac7f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac7f-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="aac7f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac7f-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aac7f-140">INPUTS</span></span>

### <span data-ttu-id="aac7f-141">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="aac7f-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="aac7f-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aac7f-142">OUTPUTS</span></span>

### <span data-ttu-id="aac7f-143">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="aac7f-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="aac7f-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aac7f-144">NOTES</span></span>

<span data-ttu-id="aac7f-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="aac7f-145">ALIASES</span></span>

<span data-ttu-id="aac7f-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="aac7f-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aac7f-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="aac7f-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aac7f-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aac7f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aac7f-149">Ana <IServer> : çoğaltmanın oluşturulacağı kaynak sunucu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="aac7f-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="aac7f-150">`Location <String>`: Kaynağın bulunduğu konum.</span><span class="sxs-lookup"><span data-stu-id="aac7f-150">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="aac7f-151">`[Tag <ITrackedResourceTags>]`: Anahtar-değer çiftleri biçiminde uygulamaya özgü meta veriler.</span><span class="sxs-lookup"><span data-stu-id="aac7f-151">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="aac7f-152">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="aac7f-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="aac7f-153">`[AdministratorLogin <String>]`: Yöneticinin sunucunun oturum açma adı.</span><span class="sxs-lookup"><span data-stu-id="aac7f-153">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="aac7f-154">Yalnızca sunucu oluşturulduğunda belirtilebilir (ve oluşturma için gereklidir).</span><span class="sxs-lookup"><span data-stu-id="aac7f-154">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="aac7f-155">`[EarliestRestoreDate <DateTime?>]`: En erken geri yükleme noktası oluşturulma zamanı (ISO8601 biçimi)</span><span class="sxs-lookup"><span data-stu-id="aac7f-155">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="aac7f-156">`[FullyQualifiedDomainName <String>]`: Sunucunun tam nitelikli etki alanı adı.</span><span class="sxs-lookup"><span data-stu-id="aac7f-156">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="aac7f-157">`[IdentityType <IdentityType?>]`: Kimlik türü.</span><span class="sxs-lookup"><span data-stu-id="aac7f-157">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="aac7f-158">Kaynak için bir Azure Active Directory sorumlusu oluşturmak ve atamak için bunu ' SystemAssigned ' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="aac7f-158">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="aac7f-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Sunucunun altyapı şifrelemesinin etkin olup olmadığını gösteren durum.</span><span class="sxs-lookup"><span data-stu-id="aac7f-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="aac7f-160">`[MasterServerId <String>]`: Bir çoğaltma sunucusunun ana sunucu kimliği.</span><span class="sxs-lookup"><span data-stu-id="aac7f-160">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="aac7f-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Sunucunun en düşük TLS sürümünü zorunlu tutun.</span><span class="sxs-lookup"><span data-stu-id="aac7f-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="aac7f-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Bu sunucuda genel ağ erişimine izin verilip verilmeyeceğini.</span><span class="sxs-lookup"><span data-stu-id="aac7f-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="aac7f-163">Değer isteğe bağlıdır, ancak geçirilirse ' Enabled ' veya ' Disabled ' olmalıdır</span><span class="sxs-lookup"><span data-stu-id="aac7f-163">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="aac7f-164">`[ReplicaCapacity <Int32?>]`: Ana sunucunun sahip olduğu en fazla yineleme sayısı.</span><span class="sxs-lookup"><span data-stu-id="aac7f-164">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="aac7f-165">`[ReplicationRole <String>]`: Sunucunun çoğaltma rolü.</span><span class="sxs-lookup"><span data-stu-id="aac7f-165">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="aac7f-166">`[SkuCapacity <Int32?>]`: Sunucunun COMPUTE birimlerini temsil eden ölçeklendirme/Out kapasitesi.</span><span class="sxs-lookup"><span data-stu-id="aac7f-166">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="aac7f-167">`[SkuFamily <String>]`: Donanım ailesi.</span><span class="sxs-lookup"><span data-stu-id="aac7f-167">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="aac7f-168">`[SkuName <String>]`: SKU 'nun adı, genellikle katman + aile + çekirdek; Örneğin, B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="aac7f-168">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="aac7f-169">`[SkuSize <String>]`: Kaynak tarafından uygun şekilde yorumlanabilecek boyut kodu.</span><span class="sxs-lookup"><span data-stu-id="aac7f-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="aac7f-170">`[SkuTier <SkuTier?>]`: Belirli SKU 'nun katmanı, örneğin. temel.</span><span class="sxs-lookup"><span data-stu-id="aac7f-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="aac7f-171">`[SslEnforcement <SslEnforcementEnum?>]`: Sunucuya bağlanırken SSL zorlamayı etkinleştir veya yok.</span><span class="sxs-lookup"><span data-stu-id="aac7f-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="aac7f-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Sunucunun yedekleme bekletme günleri.</span><span class="sxs-lookup"><span data-stu-id="aac7f-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="aac7f-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: OneDrive 'ı etkinleştir-sunucu yedeklemesi için değil.</span><span class="sxs-lookup"><span data-stu-id="aac7f-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="aac7f-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Otomatik büyüme özelliğini etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="aac7f-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="aac7f-175">`[StorageProfileStorageMb <Int32?>]`: Sunucuda izin verilen maks depolama alanı.</span><span class="sxs-lookup"><span data-stu-id="aac7f-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="aac7f-176">`[UserVisibleState <ServerState?>]`: Kullanıcının görebileceği bir sunucunun durumu.</span><span class="sxs-lookup"><span data-stu-id="aac7f-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="aac7f-177">`[Version <ServerVersion?>]`: Sunucu sürümü.</span><span class="sxs-lookup"><span data-stu-id="aac7f-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="aac7f-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aac7f-178">RELATED LINKS</span></span>

