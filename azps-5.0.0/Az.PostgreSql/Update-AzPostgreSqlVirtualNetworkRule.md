---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: a430247083e84b3d35f820b3c1e2d5f04f4979b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278497"
---
# <span data-ttu-id="e6e06-101">Update-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e6e06-101">Update-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="e6e06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6e06-102">SYNOPSIS</span></span>
<span data-ttu-id="e6e06-103">Var olan bir sanal ağ kuralını oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e6e06-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="e6e06-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6e06-104">SYNTAX</span></span>

### <span data-ttu-id="e6e06-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e6e06-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e6e06-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="e6e06-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e6e06-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6e06-107">DESCRIPTION</span></span>
<span data-ttu-id="e6e06-108">Var olan bir sanal ağ kuralını oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e6e06-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="e6e06-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6e06-109">EXAMPLES</span></span>

### <span data-ttu-id="e6e06-110">Örnek 1: PostgreSql sanal ağ kuralını adıyla güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="e6e06-110">Example 1: Update PostgreSql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default2"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="e6e06-111">Bu cmdlet, PostgreSql sanal ağ kuralını adıyla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e6e06-111">This cmdlet updates PostgreSql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="e6e06-112">Örnek 2: PostgreSql sanal ağ kuralını Identity olarak güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="e6e06-112">Example 2: Update PostgreSql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="e6e06-113">Bu cmdlet 'ler, PostgreSql sanal ağ kuralını Identity olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e6e06-113">These cmdlets update PostgreSql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="e6e06-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6e06-114">PARAMETERS</span></span>

### <span data-ttu-id="e6e06-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="e6e06-115">-AsJob</span></span>
<span data-ttu-id="e6e06-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="e6e06-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e6e06-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6e06-117">-DefaultProfile</span></span>
<span data-ttu-id="e6e06-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e6e06-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6e06-119">-Ignoremissingvnetserviceendpoint</span><span class="sxs-lookup"><span data-stu-id="e6e06-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="e6e06-120">Sanal ağın VNET hizmeti uç noktası etkinleştirilmeden önce güvenlik duvarı kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e6e06-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="e6e06-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6e06-121">-InputObject</span></span>
<span data-ttu-id="e6e06-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6e06-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6e06-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="e6e06-123">-Name</span></span>
<span data-ttu-id="e6e06-124">Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="e6e06-124">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e06-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e6e06-125">-NoWait</span></span>
<span data-ttu-id="e6e06-126">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="e6e06-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e6e06-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e6e06-127">-PassThru</span></span>
<span data-ttu-id="e6e06-128">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="e6e06-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e6e06-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6e06-129">-ResourceGroupName</span></span>
<span data-ttu-id="e6e06-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e6e06-130">The name of the resource group.</span></span>
<span data-ttu-id="e6e06-131">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="e6e06-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e6e06-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e6e06-132">-ServerName</span></span>
<span data-ttu-id="e6e06-133">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="e6e06-133">The name of the server.</span></span>

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

### <span data-ttu-id="e6e06-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e6e06-134">-SubnetId</span></span>
<span data-ttu-id="e6e06-135">Sanal ağ alt ağının ARM kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="e6e06-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="e6e06-136">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="e6e06-136">-SubscriptionId</span></span>
<span data-ttu-id="e6e06-137">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e6e06-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e6e06-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="e6e06-138">-Confirm</span></span>
<span data-ttu-id="e6e06-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e6e06-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6e06-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6e06-140">-WhatIf</span></span>
<span data-ttu-id="e6e06-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e6e06-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6e06-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e6e06-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6e06-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6e06-143">CommonParameters</span></span>
<span data-ttu-id="e6e06-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6e06-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6e06-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e6e06-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6e06-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6e06-146">INPUTS</span></span>

### <span data-ttu-id="e6e06-147">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. ıpostgresqlidentity</span><span class="sxs-lookup"><span data-stu-id="e6e06-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="e6e06-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6e06-148">OUTPUTS</span></span>

### <span data-ttu-id="e6e06-149">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. Api20171201. ıvirtualnetworkrule</span><span class="sxs-lookup"><span data-stu-id="e6e06-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="e6e06-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6e06-150">NOTES</span></span>

<span data-ttu-id="e6e06-151">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="e6e06-151">ALIASES</span></span>

<span data-ttu-id="e6e06-152">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="e6e06-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e6e06-153">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e6e06-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e6e06-154">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e6e06-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e6e06-155">INPUTOBJECT <IPostgreSqlIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="e6e06-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e6e06-156">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="e6e06-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e6e06-157">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="e6e06-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e6e06-158">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="e6e06-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e6e06-159">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="e6e06-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e6e06-160">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="e6e06-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e6e06-161">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e6e06-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e6e06-162">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="e6e06-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="e6e06-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="e6e06-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e6e06-164">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="e6e06-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e6e06-165">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e6e06-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e6e06-166">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="e6e06-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e6e06-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6e06-167">RELATED LINKS</span></span>

