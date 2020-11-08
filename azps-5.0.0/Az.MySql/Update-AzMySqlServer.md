---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: e23cc8b942033805d8ed8cd122b19e6a59bf457c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277615"
---
# <span data-ttu-id="7d59d-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="7d59d-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="7d59d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d59d-102">SYNOPSIS</span></span>
<span data-ttu-id="7d59d-103">Var olan bir sunucuyu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7d59d-103">Updates an existing server.</span></span>
<span data-ttu-id="7d59d-104">İstek gövdesi normal sunucu tanımında bulunan özelliklerin çoğuna bir tane içerebilir.</span><span class="sxs-lookup"><span data-stu-id="7d59d-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="7d59d-105">Wait_timeout veya net_retry_count gibi sunucu parametrelerini güncelleştirmek istiyorsanız Update-AzMySqlConfiguration kullanın.</span><span class="sxs-lookup"><span data-stu-id="7d59d-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="7d59d-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7d59d-106">SYNTAX</span></span>

### <span data-ttu-id="7d59d-107">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7d59d-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7d59d-108">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="7d59d-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7d59d-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="7d59d-109">DESCRIPTION</span></span>
<span data-ttu-id="7d59d-110">Var olan bir sunucuyu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7d59d-110">Updates an existing server.</span></span>
<span data-ttu-id="7d59d-111">İstek gövdesi normal sunucu tanımında bulunan özelliklerin çoğuna bir tane içerebilir.</span><span class="sxs-lookup"><span data-stu-id="7d59d-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="7d59d-112">Wait_timeout veya net_retry_count gibi sunucu parametrelerini güncelleştirmek istiyorsanız Update-AzMySqlConfiguration kullanın.</span><span class="sxs-lookup"><span data-stu-id="7d59d-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="7d59d-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7d59d-113">EXAMPLES</span></span>

### <span data-ttu-id="7d59d-114">Örnek 1: kaynak grubuna ve sunucu adına göre MySql sunucusunu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="7d59d-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="7d59d-115">Bu cmdlet, MySql sunucusunu kaynak grubuna ve sunucu adına göre güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7d59d-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="7d59d-116">Örnek 2: MySql sunucusunu Identity olarak güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="7d59d-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="7d59d-117">Bu cmdlet, MySql sunucusunu kimliğe göre güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7d59d-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="7d59d-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7d59d-118">PARAMETERS</span></span>

### <span data-ttu-id="7d59d-119">-\Administrators</span><span class="sxs-lookup"><span data-stu-id="7d59d-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="7d59d-120">Yönetici oturumunun parolası.</span><span class="sxs-lookup"><span data-stu-id="7d59d-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="7d59d-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="7d59d-121">-AsJob</span></span>
<span data-ttu-id="7d59d-122">Komutu iş olarak çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="7d59d-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="7d59d-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="7d59d-123">-BackupRetentionDay</span></span>
<span data-ttu-id="7d59d-124">Sunucu için yedekleme bekletme günleri.</span><span class="sxs-lookup"><span data-stu-id="7d59d-124">Backup retention days for the server.</span></span>
<span data-ttu-id="7d59d-125">Gün sayısı 7 ile 35 arasındadır.</span><span class="sxs-lookup"><span data-stu-id="7d59d-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="7d59d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d59d-126">-DefaultProfile</span></span>
<span data-ttu-id="7d59d-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7d59d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d59d-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d59d-128">-InputObject</span></span>
<span data-ttu-id="7d59d-129">Kimlik parametresi.</span><span class="sxs-lookup"><span data-stu-id="7d59d-129">Identity Parameter.</span></span>
<span data-ttu-id="7d59d-130">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7d59d-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d59d-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="7d59d-131">-Name</span></span>
<span data-ttu-id="7d59d-132">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="7d59d-132">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d59d-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7d59d-133">-NoWait</span></span>
<span data-ttu-id="7d59d-134">Komutu zaman uyumsuz olarak çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="7d59d-134">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="7d59d-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="7d59d-135">-ReplicationRole</span></span>
<span data-ttu-id="7d59d-136">Sunucunun çoğaltma rolü.</span><span class="sxs-lookup"><span data-stu-id="7d59d-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="7d59d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d59d-137">-ResourceGroupName</span></span>
<span data-ttu-id="7d59d-138">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7d59d-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7d59d-139">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d59d-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d59d-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="7d59d-140">-Sku</span></span>
<span data-ttu-id="7d59d-141">SKU 'nun adı, genellikle katman + aile + çekirdek; Örneğin, B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="7d59d-141">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="7d59d-142">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="7d59d-142">-SkuCapacity</span></span>
<span data-ttu-id="7d59d-143">İzleme/çıkış kapasitesi, sunucunun hesaplama birimleri 'ni temsil eder.</span><span class="sxs-lookup"><span data-stu-id="7d59d-143">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="7d59d-144">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="7d59d-144">-SkuFamily</span></span>
<span data-ttu-id="7d59d-145">Donanım ailesi.</span><span class="sxs-lookup"><span data-stu-id="7d59d-145">The family of hardware.</span></span>

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

### <span data-ttu-id="7d59d-146">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="7d59d-146">-SkuTier</span></span>
<span data-ttu-id="7d59d-147">Özel SKU 'nun katmanı, örneğin. temel.</span><span class="sxs-lookup"><span data-stu-id="7d59d-147">The tier of the particular SKU, e.g. Basic.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d59d-148">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="7d59d-148">-SslEnforcement</span></span>
<span data-ttu-id="7d59d-149">SSL zorlamayı etkinleştirme veya sunucuya bağlanırken kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="7d59d-149">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d59d-150">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="7d59d-150">-StorageAutogrow</span></span>
<span data-ttu-id="7d59d-151">Otomatik büyüme özelliğini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="7d59d-151">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d59d-152">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="7d59d-152">-StorageInMb</span></span>
<span data-ttu-id="7d59d-153">Sunucuda izin verilen maks depolama alanı.</span><span class="sxs-lookup"><span data-stu-id="7d59d-153">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="7d59d-154">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="7d59d-154">-SubscriptionId</span></span>
<span data-ttu-id="7d59d-155">Bir Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7d59d-155">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d59d-156">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7d59d-156">-Tag</span></span>
<span data-ttu-id="7d59d-157">Anahtar-değer çiftleri biçiminde uygulamaya özgü meta veriler.</span><span class="sxs-lookup"><span data-stu-id="7d59d-157">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="7d59d-158">-Onay</span><span class="sxs-lookup"><span data-stu-id="7d59d-158">-Confirm</span></span>
<span data-ttu-id="7d59d-159">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7d59d-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d59d-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d59d-160">-WhatIf</span></span>
<span data-ttu-id="7d59d-161">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7d59d-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d59d-162">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7d59d-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d59d-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d59d-163">CommonParameters</span></span>
<span data-ttu-id="7d59d-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7d59d-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d59d-165">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7d59d-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d59d-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7d59d-166">INPUTS</span></span>

### <span data-ttu-id="7d59d-167">Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Sanysqlidentity</span><span class="sxs-lookup"><span data-stu-id="7d59d-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="7d59d-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7d59d-168">OUTPUTS</span></span>

### <span data-ttu-id="7d59d-169">Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="7d59d-169">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="7d59d-170">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7d59d-170">NOTES</span></span>

<span data-ttu-id="7d59d-171">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="7d59d-171">ALIASES</span></span>

<span data-ttu-id="7d59d-172">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="7d59d-172">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7d59d-173">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7d59d-173">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7d59d-174">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7d59d-174">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7d59d-175">INPUTOBJECT <IMySqlIdentity> : IDENTITY parametresi.</span><span class="sxs-lookup"><span data-stu-id="7d59d-175">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="7d59d-176">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="7d59d-176">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="7d59d-177">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="7d59d-177">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="7d59d-178">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="7d59d-178">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="7d59d-179">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="7d59d-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7d59d-180">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="7d59d-180">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="7d59d-181">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7d59d-181">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7d59d-182">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="7d59d-182">The name is case insensitive.</span></span>
  - <span data-ttu-id="7d59d-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="7d59d-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="7d59d-184">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="7d59d-184">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="7d59d-185">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7d59d-185">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7d59d-186">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="7d59d-186">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="7d59d-187">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7d59d-187">RELATED LINKS</span></span>

