---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restore-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
ms.openlocfilehash: 49ae121273b42d3718d1a334edcaa72fa2c57583
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276577"
---
# <span data-ttu-id="39bf9-101">Restore-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="39bf9-101">Restore-AzMySqlServer</span></span>

## <span data-ttu-id="39bf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="39bf9-103">Sunucuyu mevcut bir yedekten geri yükleme</span><span class="sxs-lookup"><span data-stu-id="39bf9-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="39bf9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="39bf9-104">SYNTAX</span></span>

### <span data-ttu-id="39bf9-105">GeoRestore (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="39bf9-105">GeoRestore (Default)</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="39bf9-106">Noktalarısona erdirme</span><span class="sxs-lookup"><span data-stu-id="39bf9-106">PointInTimeRestore</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="39bf9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="39bf9-107">DESCRIPTION</span></span>
<span data-ttu-id="39bf9-108">Sunucuyu mevcut bir yedekten geri yükleme</span><span class="sxs-lookup"><span data-stu-id="39bf9-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="39bf9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="39bf9-109">EXAMPLES</span></span>

### <span data-ttu-id="39bf9-110">Örnek 1: Georeplication restore kullanarak MySql sunucusunu geri yükleme</span><span class="sxs-lookup"><span data-stu-id="39bf9-110">Example 1: Restore MySql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test-replica | Restore-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -UseGeoRestore 

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="39bf9-111">Bu cmdlet, Georeplication restore kullanarak MySql sunucusunu geri yükler.</span><span class="sxs-lookup"><span data-stu-id="39bf9-111">This cmdlet restores MySql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="39bf9-112">Örnek 2: Poinınfo kullanarak MySql sunucusunu geri yükleme</span><span class="sxs-lookup"><span data-stu-id="39bf9-112">Example 2: Restore MySql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Restore-AzMySqlServer -Name mysql-test-restore -ResourceGroupName PowershellMySqlTest -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-restore eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="39bf9-113">Bu cmdlet 'ler, PointInTime restore kullanarak MySql sunucusunu geri yükler.</span><span class="sxs-lookup"><span data-stu-id="39bf9-113">These cmdlets restore MySql server using PointInTime Restore.</span></span>

## <span data-ttu-id="39bf9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="39bf9-114">PARAMETERS</span></span>

### <span data-ttu-id="39bf9-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="39bf9-115">-AsJob</span></span>
<span data-ttu-id="39bf9-116">Komutu iş olarak çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="39bf9-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="39bf9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39bf9-117">-DefaultProfile</span></span>
<span data-ttu-id="39bf9-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="39bf9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39bf9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39bf9-119">-InputObject</span></span>
<span data-ttu-id="39bf9-120">Geri yüklenecek kaynak sunucu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="39bf9-120">The source server object to restore from.</span></span>
<span data-ttu-id="39bf9-121">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="39bf9-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39bf9-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="39bf9-122">-Location</span></span>
<span data-ttu-id="39bf9-123">Kaynağın bulunduğu konum.</span><span class="sxs-lookup"><span data-stu-id="39bf9-123">The location the resource resides in.</span></span>

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

### <span data-ttu-id="39bf9-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="39bf9-124">-Name</span></span>
<span data-ttu-id="39bf9-125">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="39bf9-125">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bf9-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="39bf9-126">-NoWait</span></span>
<span data-ttu-id="39bf9-127">Komutu zaman uyumsuz olarak çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="39bf9-127">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="39bf9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39bf9-128">-ResourceGroupName</span></span>
<span data-ttu-id="39bf9-129">Kaynağı içeren kaynak grubunun adı, bu değeri Azure Kaynak Yöneticisi API 'sinden veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="39bf9-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="39bf9-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="39bf9-130">-RestorePointInTime</span></span>
<span data-ttu-id="39bf9-131">Kaynağın bulunduğu konum.</span><span class="sxs-lookup"><span data-stu-id="39bf9-131">The location the resource resides in.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bf9-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="39bf9-132">-Sku</span></span>
<span data-ttu-id="39bf9-133">SKU 'nun adı, genellikle katman + aile + çekirdek; Örneğin, B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="39bf9-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="39bf9-134">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="39bf9-134">-SubscriptionId</span></span>
<span data-ttu-id="39bf9-135">Bir Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="39bf9-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="39bf9-136">Etiketli</span><span class="sxs-lookup"><span data-stu-id="39bf9-136">-Tag</span></span>
<span data-ttu-id="39bf9-137">Anahtar-değer çiftleri biçiminde uygulamaya özgü meta veriler.</span><span class="sxs-lookup"><span data-stu-id="39bf9-137">Application-specific metadata in the form of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bf9-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="39bf9-138">-UseGeoRestore</span></span>
<span data-ttu-id="39bf9-139">Geri yüklemek için coğrafi modu kullanma</span><span class="sxs-lookup"><span data-stu-id="39bf9-139">Use Geo mode to restore</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bf9-140">-Usepointintimeresiz</span><span class="sxs-lookup"><span data-stu-id="39bf9-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="39bf9-141">Geri yükleme</span><span class="sxs-lookup"><span data-stu-id="39bf9-141">Use PointInTime mode to restore</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bf9-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="39bf9-142">-Confirm</span></span>
<span data-ttu-id="39bf9-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="39bf9-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39bf9-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39bf9-144">-WhatIf</span></span>
<span data-ttu-id="39bf9-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="39bf9-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39bf9-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="39bf9-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39bf9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39bf9-147">CommonParameters</span></span>
<span data-ttu-id="39bf9-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="39bf9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39bf9-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="39bf9-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39bf9-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="39bf9-150">INPUTS</span></span>

### <span data-ttu-id="39bf9-151">Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="39bf9-151">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="39bf9-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="39bf9-152">OUTPUTS</span></span>

### <span data-ttu-id="39bf9-153">Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="39bf9-153">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="39bf9-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="39bf9-154">NOTES</span></span>

<span data-ttu-id="39bf9-155">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="39bf9-155">ALIASES</span></span>

<span data-ttu-id="39bf9-156">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="39bf9-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="39bf9-157">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="39bf9-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="39bf9-158">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="39bf9-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="39bf9-159">INPUTOBJECT <IServer> : geri yüklenecek kaynak sunucu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="39bf9-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="39bf9-160">`Location <String>`: Kaynağın bulunduğu konum.</span><span class="sxs-lookup"><span data-stu-id="39bf9-160">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="39bf9-161">`[Tag <ITrackedResourceTags>]`: Anahtar-değer çiftleri biçiminde uygulamaya özgü meta veriler.</span><span class="sxs-lookup"><span data-stu-id="39bf9-161">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="39bf9-162">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="39bf9-162">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="39bf9-163">`[AdministratorLogin <String>]`: Yöneticinin sunucunun oturum açma adı.</span><span class="sxs-lookup"><span data-stu-id="39bf9-163">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="39bf9-164">Yalnızca sunucu oluşturulduğunda belirtilebilir (ve oluşturma için gereklidir).</span><span class="sxs-lookup"><span data-stu-id="39bf9-164">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="39bf9-165">`[EarliestRestoreDate <DateTime?>]`: En erken geri yükleme noktası oluşturulma zamanı (ISO8601 biçimi)</span><span class="sxs-lookup"><span data-stu-id="39bf9-165">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="39bf9-166">`[FullyQualifiedDomainName <String>]`: Sunucunun tam nitelikli etki alanı adı.</span><span class="sxs-lookup"><span data-stu-id="39bf9-166">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="39bf9-167">`[IdentityType <IdentityType?>]`: Kimlik türü.</span><span class="sxs-lookup"><span data-stu-id="39bf9-167">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="39bf9-168">Kaynak için bir Azure Active Directory sorumlusu oluşturmak ve atamak için bunu ' SystemAssigned ' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="39bf9-168">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="39bf9-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Sunucunun altyapı şifrelemesinin etkin olup olmadığını gösteren durum.</span><span class="sxs-lookup"><span data-stu-id="39bf9-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="39bf9-170">`[MasterServerId <String>]`: Bir çoğaltma sunucusunun ana sunucu kimliği.</span><span class="sxs-lookup"><span data-stu-id="39bf9-170">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="39bf9-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Sunucunun en düşük TLS sürümünü zorunlu tutun.</span><span class="sxs-lookup"><span data-stu-id="39bf9-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="39bf9-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Bu sunucuda genel ağ erişimine izin verilip verilmeyeceğini.</span><span class="sxs-lookup"><span data-stu-id="39bf9-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="39bf9-173">Değer isteğe bağlıdır, ancak geçirilirse ' Enabled ' veya ' Disabled ' olmalıdır</span><span class="sxs-lookup"><span data-stu-id="39bf9-173">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="39bf9-174">`[ReplicaCapacity <Int32?>]`: Ana sunucunun sahip olduğu en fazla yineleme sayısı.</span><span class="sxs-lookup"><span data-stu-id="39bf9-174">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="39bf9-175">`[ReplicationRole <String>]`: Sunucunun çoğaltma rolü.</span><span class="sxs-lookup"><span data-stu-id="39bf9-175">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="39bf9-176">`[SkuCapacity <Int32?>]`: Sunucunun COMPUTE birimlerini temsil eden ölçeklendirme/Out kapasitesi.</span><span class="sxs-lookup"><span data-stu-id="39bf9-176">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="39bf9-177">`[SkuFamily <String>]`: Donanım ailesi.</span><span class="sxs-lookup"><span data-stu-id="39bf9-177">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="39bf9-178">`[SkuName <String>]`: SKU 'nun adı, genellikle katman + aile + çekirdek; Örneğin, B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="39bf9-178">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="39bf9-179">`[SkuSize <String>]`: Kaynak tarafından uygun şekilde yorumlanabilecek boyut kodu.</span><span class="sxs-lookup"><span data-stu-id="39bf9-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="39bf9-180">`[SkuTier <SkuTier?>]`: Belirli SKU 'nun katmanı, örneğin. temel.</span><span class="sxs-lookup"><span data-stu-id="39bf9-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="39bf9-181">`[SslEnforcement <SslEnforcementEnum?>]`: Sunucuya bağlanırken SSL zorlamayı etkinleştir veya yok.</span><span class="sxs-lookup"><span data-stu-id="39bf9-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="39bf9-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Sunucunun yedekleme bekletme günleri.</span><span class="sxs-lookup"><span data-stu-id="39bf9-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="39bf9-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: OneDrive 'ı etkinleştir-sunucu yedeklemesi için değil.</span><span class="sxs-lookup"><span data-stu-id="39bf9-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="39bf9-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Otomatik büyüme özelliğini etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="39bf9-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="39bf9-185">`[StorageProfileStorageMb <Int32?>]`: Sunucuda izin verilen maks depolama alanı.</span><span class="sxs-lookup"><span data-stu-id="39bf9-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="39bf9-186">`[UserVisibleState <ServerState?>]`: Kullanıcının görebileceği bir sunucunun durumu.</span><span class="sxs-lookup"><span data-stu-id="39bf9-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="39bf9-187">`[Version <ServerVersion?>]`: Sunucu sürümü.</span><span class="sxs-lookup"><span data-stu-id="39bf9-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="39bf9-188">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="39bf9-188">RELATED LINKS</span></span>

