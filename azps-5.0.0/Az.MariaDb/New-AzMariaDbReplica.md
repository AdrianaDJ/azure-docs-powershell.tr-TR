---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 0ce25af607d2460abf2ec4585dacc124a1f2e65c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278648"
---
# <span data-ttu-id="6b2c5-101">New-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="6b2c5-101">New-AzMariaDbReplica</span></span>

## <span data-ttu-id="6b2c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b2c5-102">SYNOPSIS</span></span>
<span data-ttu-id="6b2c5-103">MariaDB sunucusunun yinelemesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-103">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="6b2c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b2c5-104">SYNTAX</span></span>

### <span data-ttu-id="6b2c5-105">ServerName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6b2c5-105">ServerName (Default)</span></span>
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6b2c5-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="6b2c5-106">ServerObject</span></span>
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="6b2c5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b2c5-107">DESCRIPTION</span></span>
<span data-ttu-id="6b2c5-108">MariaDB sunucusunun yinelemesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-108">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="6b2c5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b2c5-109">EXAMPLES</span></span>

### <span data-ttu-id="6b2c5-110">Örnek 1: MariaDB için çoğaltma DB oluşturma</span><span class="sxs-lookup"><span data-stu-id="6b2c5-110">Example 1: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="6b2c5-111">Bu komut, bir MariaDB için bir çoğaltma DB oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-111">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="6b2c5-112">Örnek 2: bir Mari</span><span class="sxs-lookup"><span data-stu-id="6b2c5-112">Example 2: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="6b2c5-113">Bu komut, bir MariaDB için bir çoğaltma DB oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-113">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="6b2c5-114">Örnek 3: bir Mari</span><span class="sxs-lookup"><span data-stu-id="6b2c5-114">Example 3: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="6b2c5-115">Bu komut InputObject parametresi, bir MariaDB parametresi InputObject parametresine sahip bir çoğaltma DB oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-115">This command with parameter inputobject creates a replica db with parameter inputobject for a MariaDB.</span></span>

## <span data-ttu-id="6b2c5-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b2c5-116">PARAMETERS</span></span>

### <span data-ttu-id="6b2c5-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="6b2c5-117">-AsJob</span></span>
<span data-ttu-id="6b2c5-118">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="6b2c5-118">Run the command as a job</span></span>

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

### <span data-ttu-id="6b2c5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b2c5-119">-DefaultProfile</span></span>
<span data-ttu-id="6b2c5-120">bölge DefaultParameters Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b2c5-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="6b2c5-121">-Location</span></span>
<span data-ttu-id="6b2c5-122">Kaynağın bulunduğu konum.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-122">The location the resource resides in.</span></span>

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

### <span data-ttu-id="6b2c5-123">-Master</span><span class="sxs-lookup"><span data-stu-id="6b2c5-123">-Master</span></span>
<span data-ttu-id="6b2c5-124">Geri yüklenecek kaynak sunucu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-124">The source server object to restore from.</span></span>
<span data-ttu-id="6b2c5-125">Oluşturmak için, ana özellikler için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-125">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2c5-126">-MasterName</span><span class="sxs-lookup"><span data-stu-id="6b2c5-126">-MasterName</span></span>
<span data-ttu-id="6b2c5-127">MariaDB sunucu adı.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-127">MariaDB server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b2c5-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6b2c5-128">-NoWait</span></span>
<span data-ttu-id="6b2c5-129">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="6b2c5-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6b2c5-130">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="6b2c5-130">-ReplicaName</span></span>
<span data-ttu-id="6b2c5-131">Çoğaltma adı.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-131">Replica name.</span></span>

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

### <span data-ttu-id="6b2c5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b2c5-132">-ResourceGroupName</span></span>
<span data-ttu-id="6b2c5-133">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b2c5-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="6b2c5-134">-Sku</span></span>
<span data-ttu-id="6b2c5-135">SKU 'nun adı, genellikle katman + aile + çekirdek; Örneğin, B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-135">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="6b2c5-136">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="6b2c5-136">-SubscriptionId</span></span>
<span data-ttu-id="6b2c5-137">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-137">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6b2c5-138">Etiketli</span><span class="sxs-lookup"><span data-stu-id="6b2c5-138">-Tag</span></span>
<span data-ttu-id="6b2c5-139">Anahtar-değer çiftleri biçiminde uygulamaya özgü meta veriler.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-139">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="6b2c5-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="6b2c5-140">-Confirm</span></span>
<span data-ttu-id="6b2c5-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b2c5-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b2c5-142">-WhatIf</span></span>
<span data-ttu-id="6b2c5-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b2c5-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b2c5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b2c5-145">CommonParameters</span></span>
<span data-ttu-id="6b2c5-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b2c5-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b2c5-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b2c5-148">INPUTS</span></span>

### <span data-ttu-id="6b2c5-149">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="6b2c5-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="6b2c5-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b2c5-150">OUTPUTS</span></span>

### <span data-ttu-id="6b2c5-151">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="6b2c5-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="6b2c5-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b2c5-152">NOTES</span></span>

<span data-ttu-id="6b2c5-153">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="6b2c5-153">ALIASES</span></span>

<span data-ttu-id="6b2c5-154">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="6b2c5-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6b2c5-155">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b2c5-156">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6b2c5-157">Ana <IServer> : geri yüklenecek kaynak sunucu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-157">MASTER <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="6b2c5-158">`Location <String>`: Kaynağın bulunduğu konum.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-158">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="6b2c5-159">`[Tag <ITrackedResourceTags>]`: Anahtar-değer çiftleri biçiminde uygulamaya özgü meta veriler.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-159">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="6b2c5-160">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="6b2c5-161">`[AdministratorLogin <String>]`: Yöneticinin sunucunun oturum açma adı.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-161">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="6b2c5-162">Yalnızca sunucu oluşturulduğunda belirtilebilir (ve oluşturma için gereklidir).</span><span class="sxs-lookup"><span data-stu-id="6b2c5-162">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="6b2c5-163">`[EarliestRestoreDate <DateTime?>]`: En erken geri yükleme noktası oluşturulma zamanı (ISO8601 biçimi)</span><span class="sxs-lookup"><span data-stu-id="6b2c5-163">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="6b2c5-164">`[FullyQualifiedDomainName <String>]`: Sunucunun tam nitelikli etki alanı adı.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-164">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="6b2c5-165">`[IdentityType <IdentityType?>]`: Kimlik türü.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-165">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="6b2c5-166">Kaynak için bir Azure Active Directory sorumlusu oluşturmak ve atamak için bunu ' SystemAssigned ' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-166">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="6b2c5-167">`[MasterServerId <String>]`: Bir çoğaltma sunucusunun ana sunucu kimliği.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-167">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="6b2c5-168">`[ReplicaCapacity <Int32?>]`: Ana sunucunun sahip olduğu en fazla yineleme sayısı.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-168">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="6b2c5-169">`[ReplicationRole <String>]`: Sunucunun çoğaltma rolü.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-169">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="6b2c5-170">`[SkuCapacity <Int32?>]`: Sunucunun COMPUTE birimlerini temsil eden ölçeklendirme/Out kapasitesi.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-170">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="6b2c5-171">`[SkuFamily <String>]`: Donanım ailesi.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-171">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="6b2c5-172">`[SkuName <String>]`: SKU 'nun adı, genellikle katman + aile + çekirdek; Örneğin, B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-172">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="6b2c5-173">`[SkuSize <String>]`: Kaynak tarafından uygun şekilde yorumlanabilecek boyut kodu.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-173">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="6b2c5-174">`[SkuTier <SkuTier?>]`: Belirli SKU 'nun katmanı, örneğin. temel.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-174">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="6b2c5-175">`[SslEnforcement <SslEnforcementEnum?>]`: Sunucuya bağlanırken SSL zorlamayı etkinleştir veya yok.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-175">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="6b2c5-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Sunucunun yedekleme bekletme günleri.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="6b2c5-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: OneDrive 'ı etkinleştir-sunucu yedeklemesi için değil.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="6b2c5-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Otomatik büyüme özelliğini etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="6b2c5-179">`[StorageProfileStorageMb <Int32?>]`: Sunucuda izin verilen maks depolama alanı.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-179">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="6b2c5-180">`[UserVisibleState <ServerState?>]`: Kullanıcının görebileceği bir sunucunun durumu.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-180">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="6b2c5-181">`[Version <ServerVersion?>]`: Sunucu sürümü.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-181">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="6b2c5-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b2c5-182">RELATED LINKS</span></span>

