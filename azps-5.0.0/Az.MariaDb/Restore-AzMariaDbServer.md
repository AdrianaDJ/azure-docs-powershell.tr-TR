---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restore-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
ms.openlocfilehash: 95988d83cbb4c3dcf0b5da890bf38f8c40eb4dfa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280093"
---
# <span data-ttu-id="01325-101">Restore-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="01325-101">Restore-AzMariaDbServer</span></span>

## <span data-ttu-id="01325-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01325-102">SYNOPSIS</span></span>
<span data-ttu-id="01325-103">Var olan bir Mari.</span><span class="sxs-lookup"><span data-stu-id="01325-103">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="01325-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01325-104">SYNTAX</span></span>

```
Restore-AzMariaDbServer -Name <String> -RestorePointInTime <DateTime> [-InputObject <IServer>]
 [-ResourceGroupName <String>] [-ServerName <String>] [-SubscriptionId <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="01325-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="01325-105">DESCRIPTION</span></span>
<span data-ttu-id="01325-106">Var olan bir Mari.</span><span class="sxs-lookup"><span data-stu-id="01325-106">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="01325-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01325-107">EXAMPLES</span></span>

### <span data-ttu-id="01325-108">Örnek 1: sunucu adına bir PointInTime MariaDB öğesini geri yükleyin.</span><span class="sxs-lookup"><span data-stu-id="01325-108">Example 1: Restore a PointInTime MariaDB by server name.</span></span>
```powershell
PS C:\> Restore-AzMariaDbServer -Name restore-db01 -ServerName mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db01 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="01325-109">Bu komut, bir Poinıntime MariaDB 'yi sunucu adına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="01325-109">This command restore a PointInTime MariaDB by server name.</span></span>

### <span data-ttu-id="01325-110">Örnek 2: sunucu nesnesine göre pointintime Mari</span><span class="sxs-lookup"><span data-stu-id="01325-110">Example 2: Restore a PointInTime MariaDB by server object</span></span>
```powershell
PS C:\> $db = Get-AzMariaDbServer -Name mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z
PS C:\>Restore-AzMariaDbServer -Name restore-db02 -InputObject $db -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db02 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="01325-111">Bu komut, sunucu nesnesine bir PointInTime MariaDB geri yükler.</span><span class="sxs-lookup"><span data-stu-id="01325-111">This command restore a PointInTime MariaDB by server object.</span></span>

## <span data-ttu-id="01325-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01325-112">PARAMETERS</span></span>

### <span data-ttu-id="01325-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="01325-113">-AsJob</span></span>
<span data-ttu-id="01325-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="01325-114">Run the command as a job</span></span>

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

### <span data-ttu-id="01325-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01325-115">-DefaultProfile</span></span>
<span data-ttu-id="01325-116">bölge DefaultParameters Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="01325-116">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01325-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01325-117">-InputObject</span></span>
<span data-ttu-id="01325-118">Geri yüklenecek kaynak sunucu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="01325-118">The source server object to restore from.</span></span>
<span data-ttu-id="01325-119">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="01325-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01325-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="01325-120">-Location</span></span>
<span data-ttu-id="01325-121">Kaynağın bulunduğu konum.</span><span class="sxs-lookup"><span data-stu-id="01325-121">The location the resource resides in.</span></span>

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

### <span data-ttu-id="01325-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="01325-122">-Name</span></span>
<span data-ttu-id="01325-123">Geri yüklenecek hedef sunucu adı.</span><span class="sxs-lookup"><span data-stu-id="01325-123">The dest server name to restore from.</span></span>

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

### <span data-ttu-id="01325-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="01325-124">-NoWait</span></span>
<span data-ttu-id="01325-125">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="01325-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="01325-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01325-126">-ResourceGroupName</span></span>
<span data-ttu-id="01325-127">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="01325-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="01325-128">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01325-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="01325-129">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="01325-129">-RestorePointInTime</span></span>
<span data-ttu-id="01325-130">bölge Poinıntimer, kaynağın bulunduğu konumu alır.</span><span class="sxs-lookup"><span data-stu-id="01325-130">region PointInTimeRestore The location the resource resides in.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01325-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="01325-131">-ServerName</span></span>
<span data-ttu-id="01325-132">Geri yüklenecek kaynak sunucu adı.</span><span class="sxs-lookup"><span data-stu-id="01325-132">The source server name to restore from.</span></span>

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

### <span data-ttu-id="01325-133">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="01325-133">-SubscriptionId</span></span>
<span data-ttu-id="01325-134">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="01325-134">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="01325-135">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="01325-135">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="01325-136">Etiketli</span><span class="sxs-lookup"><span data-stu-id="01325-136">-Tag</span></span>
<span data-ttu-id="01325-137">Anahtar-değer çiftleri biçiminde uygulamaya özgü meta veriler.</span><span class="sxs-lookup"><span data-stu-id="01325-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="01325-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="01325-138">-Confirm</span></span>
<span data-ttu-id="01325-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="01325-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01325-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01325-140">-WhatIf</span></span>
<span data-ttu-id="01325-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="01325-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01325-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="01325-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01325-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01325-143">CommonParameters</span></span>
<span data-ttu-id="01325-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01325-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01325-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="01325-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01325-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01325-146">INPUTS</span></span>

### <span data-ttu-id="01325-147">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="01325-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="01325-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01325-148">OUTPUTS</span></span>

### <span data-ttu-id="01325-149">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="01325-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="01325-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01325-150">NOTES</span></span>

<span data-ttu-id="01325-151">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="01325-151">ALIASES</span></span>

<span data-ttu-id="01325-152">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="01325-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="01325-153">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="01325-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="01325-154">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="01325-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="01325-155">INPUTOBJECT <IServer> : geri yüklenecek kaynak sunucu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="01325-155">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="01325-156">`Location <String>`: Kaynağın bulunduğu konum.</span><span class="sxs-lookup"><span data-stu-id="01325-156">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="01325-157">`[Tag <ITrackedResourceTags>]`: Anahtar-değer çiftleri biçiminde uygulamaya özgü meta veriler.</span><span class="sxs-lookup"><span data-stu-id="01325-157">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="01325-158">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="01325-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="01325-159">`[AdministratorLogin <String>]`: Yöneticinin sunucunun oturum açma adı.</span><span class="sxs-lookup"><span data-stu-id="01325-159">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="01325-160">Yalnızca sunucu oluşturulduğunda belirtilebilir (ve oluşturma için gereklidir).</span><span class="sxs-lookup"><span data-stu-id="01325-160">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="01325-161">`[EarliestRestoreDate <DateTime?>]`: En erken geri yükleme noktası oluşturulma zamanı (ISO8601 biçimi)</span><span class="sxs-lookup"><span data-stu-id="01325-161">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="01325-162">`[FullyQualifiedDomainName <String>]`: Sunucunun tam nitelikli etki alanı adı.</span><span class="sxs-lookup"><span data-stu-id="01325-162">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="01325-163">`[IdentityType <IdentityType?>]`: Kimlik türü.</span><span class="sxs-lookup"><span data-stu-id="01325-163">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="01325-164">Kaynak için bir Azure Active Directory sorumlusu oluşturmak ve atamak için bunu ' SystemAssigned ' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="01325-164">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="01325-165">`[MasterServerId <String>]`: Bir çoğaltma sunucusunun ana sunucu kimliği.</span><span class="sxs-lookup"><span data-stu-id="01325-165">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="01325-166">`[ReplicaCapacity <Int32?>]`: Ana sunucunun sahip olduğu en fazla yineleme sayısı.</span><span class="sxs-lookup"><span data-stu-id="01325-166">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="01325-167">`[ReplicationRole <String>]`: Sunucunun çoğaltma rolü.</span><span class="sxs-lookup"><span data-stu-id="01325-167">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="01325-168">`[SkuCapacity <Int32?>]`: Sunucunun COMPUTE birimlerini temsil eden ölçeklendirme/Out kapasitesi.</span><span class="sxs-lookup"><span data-stu-id="01325-168">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="01325-169">`[SkuFamily <String>]`: Donanım ailesi.</span><span class="sxs-lookup"><span data-stu-id="01325-169">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="01325-170">`[SkuName <String>]`: SKU 'nun adı, genellikle katman + aile + çekirdek; Örneğin, B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="01325-170">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="01325-171">`[SkuSize <String>]`: Kaynak tarafından uygun şekilde yorumlanabilecek boyut kodu.</span><span class="sxs-lookup"><span data-stu-id="01325-171">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="01325-172">`[SkuTier <SkuTier?>]`: Belirli SKU 'nun katmanı, örneğin. temel.</span><span class="sxs-lookup"><span data-stu-id="01325-172">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="01325-173">`[SslEnforcement <SslEnforcementEnum?>]`: Sunucuya bağlanırken SSL zorlamayı etkinleştir veya yok.</span><span class="sxs-lookup"><span data-stu-id="01325-173">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="01325-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Sunucunun yedekleme bekletme günleri.</span><span class="sxs-lookup"><span data-stu-id="01325-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="01325-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: OneDrive 'ı etkinleştir-sunucu yedeklemesi için değil.</span><span class="sxs-lookup"><span data-stu-id="01325-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="01325-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Otomatik büyüme özelliğini etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="01325-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="01325-177">`[StorageProfileStorageMb <Int32?>]`: Sunucuda izin verilen maks depolama alanı.</span><span class="sxs-lookup"><span data-stu-id="01325-177">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="01325-178">`[UserVisibleState <ServerState?>]`: Kullanıcının görebileceği bir sunucunun durumu.</span><span class="sxs-lookup"><span data-stu-id="01325-178">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="01325-179">`[Version <ServerVersion?>]`: Sunucu sürümü.</span><span class="sxs-lookup"><span data-stu-id="01325-179">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="01325-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01325-180">RELATED LINKS</span></span>

