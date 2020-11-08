---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
ms.openlocfilehash: 0a6286c7574a2bf7226f8d4b80a5cac62c535a47
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280090"
---
# <span data-ttu-id="40c75-101">Update-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="40c75-101">Update-AzMariaDbServer</span></span>

## <span data-ttu-id="40c75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40c75-102">SYNOPSIS</span></span>
<span data-ttu-id="40c75-103">Var olan bir sunucuyu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="40c75-103">Updates an existing server.</span></span>
<span data-ttu-id="40c75-104">İstek gövdesi normal sunucu tanımında bulunan özelliklerin çoğuna bir tane içerebilir.</span><span class="sxs-lookup"><span data-stu-id="40c75-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="40c75-105">Wait_timeout veya net_retry_count gibi sunucu parametrelerini güncelleştirmek istiyorsanız Update-AzMariaDbConfiguration kullanın.</span><span class="sxs-lookup"><span data-stu-id="40c75-105">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="40c75-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40c75-106">SYNTAX</span></span>

### <span data-ttu-id="40c75-107">ServerName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="40c75-107">ServerName (Default)</span></span>
```
Update-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>] [-Sku <String>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="40c75-108">ServerObject</span><span class="sxs-lookup"><span data-stu-id="40c75-108">ServerObject</span></span>
```
Update-AzMariaDbServer -InputObject <IMariaDbIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>]
 [-Sku <String>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="40c75-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="40c75-109">DESCRIPTION</span></span>
<span data-ttu-id="40c75-110">Var olan bir sunucuyu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="40c75-110">Updates an existing server.</span></span>
<span data-ttu-id="40c75-111">İstek gövdesi normal sunucu tanımında bulunan özelliklerin çoğuna bir tane içerebilir.</span><span class="sxs-lookup"><span data-stu-id="40c75-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="40c75-112">Wait_timeout veya net_retry_count gibi sunucu parametrelerini güncelleştirmek istiyorsanız Update-AzMariaDbConfiguration kullanın.</span><span class="sxs-lookup"><span data-stu-id="40c75-112">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="40c75-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40c75-113">EXAMPLES</span></span>

### <span data-ttu-id="40c75-114">Örnek 1: Mari</span><span class="sxs-lookup"><span data-stu-id="40c75-114">Example 1: Update MariaDB</span></span>
```powershell
PS C:\> Update-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StorageInMb 8192

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    8192                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="40c75-115">Bu komut bir Mari.</span><span class="sxs-lookup"><span data-stu-id="40c75-115">This command updates a MariaDB.</span></span>

### <span data-ttu-id="40c75-116">Örnek 2: MariaDB 'yi güncelleyin</span><span class="sxs-lookup"><span data-stu-id="40c75-116">Example 2: Update MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 | Update-AzMariaDbServer -StorageInMb (8192+1024)

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    9216                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="40c75-117">Bu komut bir Mari.</span><span class="sxs-lookup"><span data-stu-id="40c75-117">This command updates a MariaDB.</span></span>

## <span data-ttu-id="40c75-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40c75-118">PARAMETERS</span></span>

### <span data-ttu-id="40c75-119">-\Administrators</span><span class="sxs-lookup"><span data-stu-id="40c75-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="40c75-120">Yönetici oturumunun parolası.</span><span class="sxs-lookup"><span data-stu-id="40c75-120">The password of the administrator login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c75-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="40c75-121">-AsJob</span></span>
<span data-ttu-id="40c75-122">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="40c75-122">Run the command as a job</span></span>

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

### <span data-ttu-id="40c75-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="40c75-123">-BackupRetentionDay</span></span>
<span data-ttu-id="40c75-124">Sunucu için yedekleme bekletme günleri.</span><span class="sxs-lookup"><span data-stu-id="40c75-124">Backup retention days for the server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c75-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c75-125">-DefaultProfile</span></span>
<span data-ttu-id="40c75-126">bölge DefaultParameters Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="40c75-126">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40c75-127">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="40c75-127">-GeoRedundantBackup</span></span>
<span data-ttu-id="40c75-128">Coğrafi olarak yedekli veya sunucu yedeklemesi için değil özelliğini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="40c75-128">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c75-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40c75-129">-InputObject</span></span>
<span data-ttu-id="40c75-130">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="40c75-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40c75-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="40c75-131">-Name</span></span>
<span data-ttu-id="40c75-132">MariaDB sunucu adı</span><span class="sxs-lookup"><span data-stu-id="40c75-132">MariaDB server name</span></span>

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

### <span data-ttu-id="40c75-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="40c75-133">-NoWait</span></span>
<span data-ttu-id="40c75-134">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="40c75-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="40c75-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="40c75-135">-ReplicationRole</span></span>
<span data-ttu-id="40c75-136">Sunucunun çoğaltma rolü.</span><span class="sxs-lookup"><span data-stu-id="40c75-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="40c75-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40c75-137">-ResourceGroupName</span></span>
<span data-ttu-id="40c75-138">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="40c75-138">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="40c75-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="40c75-139">-Sku</span></span>
<span data-ttu-id="40c75-140">SKU 'nun adı, genellikle katman + aile + çekirdek; Örneğin, B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="40c75-140">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="40c75-141">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="40c75-141">-SslEnforcement</span></span>
<span data-ttu-id="40c75-142">SSL zorlamayı etkinleştirme veya sunucuya bağlanırken kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="40c75-142">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c75-143">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="40c75-143">-StorageAutogrow</span></span>
<span data-ttu-id="40c75-144">Otomatik büyüme özelliğini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="40c75-144">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c75-145">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="40c75-145">-StorageInMb</span></span>
<span data-ttu-id="40c75-146">Sunucuda izin verilen maks depolama alanı.</span><span class="sxs-lookup"><span data-stu-id="40c75-146">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c75-147">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="40c75-147">-SubscriptionId</span></span>
<span data-ttu-id="40c75-148">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır</span><span class="sxs-lookup"><span data-stu-id="40c75-148">The subscription ID is part of the URI for every service call</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c75-149">Etiketli</span><span class="sxs-lookup"><span data-stu-id="40c75-149">-Tag</span></span>
<span data-ttu-id="40c75-150">Anahtar-değer çiftleri biçiminde uygulamaya özgü meta veriler.</span><span class="sxs-lookup"><span data-stu-id="40c75-150">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="40c75-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="40c75-151">-Confirm</span></span>
<span data-ttu-id="40c75-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="40c75-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40c75-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40c75-153">-WhatIf</span></span>
<span data-ttu-id="40c75-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="40c75-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40c75-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="40c75-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40c75-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c75-156">CommonParameters</span></span>
<span data-ttu-id="40c75-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40c75-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c75-158">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="40c75-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40c75-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40c75-159">INPUTS</span></span>

### <span data-ttu-id="40c75-160">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Sanarladbıdentity</span><span class="sxs-lookup"><span data-stu-id="40c75-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="40c75-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40c75-161">OUTPUTS</span></span>

### <span data-ttu-id="40c75-162">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="40c75-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="40c75-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40c75-163">NOTES</span></span>

<span data-ttu-id="40c75-164">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="40c75-164">ALIASES</span></span>

<span data-ttu-id="40c75-165">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="40c75-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="40c75-166">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="40c75-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="40c75-167">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="40c75-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="40c75-168">INPUTOBJECT <IMariaDbIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="40c75-168">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="40c75-169">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="40c75-169">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="40c75-170">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="40c75-170">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="40c75-171">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="40c75-171">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="40c75-172">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="40c75-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="40c75-173">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="40c75-173">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="40c75-174">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="40c75-174">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="40c75-175">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="40c75-175">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="40c75-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="40c75-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="40c75-177">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="40c75-177">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="40c75-178">`[SubscriptionId <String>]`: Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="40c75-178">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="40c75-179">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="40c75-179">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="40c75-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40c75-180">RELATED LINKS</span></span>

