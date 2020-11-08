---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 9ec9113ba17ec28e7cef934a4b857e4cbf0acce0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274452"
---
# <span data-ttu-id="46107-101">Update-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="46107-101">Update-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="46107-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46107-102">SYNOPSIS</span></span>
<span data-ttu-id="46107-103">Var olan bir sanal ağ kuralını oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="46107-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="46107-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46107-104">SYNTAX</span></span>

### <span data-ttu-id="46107-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="46107-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="46107-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="46107-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-IgnoreMissingVnetServiceEndpoint]
 [-SubnetId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="46107-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="46107-107">DESCRIPTION</span></span>
<span data-ttu-id="46107-108">Var olan bir sanal ağ kuralını oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="46107-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="46107-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46107-109">EXAMPLES</span></span>

### <span data-ttu-id="46107-110">Örnek 1: MariaDB sanal ağ kuralını Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="46107-110">Example 1: Update MariaDB virtual network rule</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> Update-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnetrule-QdMJpU -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="46107-111">Bu komut, sanal ağ kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="46107-111">This command updates a virtual network rule.</span></span>

## <span data-ttu-id="46107-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46107-112">PARAMETERS</span></span>

### <span data-ttu-id="46107-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="46107-113">-AsJob</span></span>
<span data-ttu-id="46107-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="46107-114">Run the command as a job</span></span>

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

### <span data-ttu-id="46107-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46107-115">-DefaultProfile</span></span>
<span data-ttu-id="46107-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="46107-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46107-117">-Ignoremissingvnetserviceendpoint</span><span class="sxs-lookup"><span data-stu-id="46107-117">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="46107-118">Sanal ağın VNET hizmeti uç noktası etkinleştirilmeden önce güvenlik duvarı kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="46107-118">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="46107-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46107-119">-InputObject</span></span>
<span data-ttu-id="46107-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="46107-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46107-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="46107-121">-Name</span></span>
<span data-ttu-id="46107-122">Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="46107-122">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="46107-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="46107-123">-NoWait</span></span>
<span data-ttu-id="46107-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="46107-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="46107-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="46107-125">-PassThru</span></span>
<span data-ttu-id="46107-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="46107-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="46107-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46107-127">-ResourceGroupName</span></span>
<span data-ttu-id="46107-128">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="46107-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="46107-129">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46107-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="46107-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="46107-130">-ServerName</span></span>
<span data-ttu-id="46107-131">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="46107-131">The name of the server.</span></span>

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

### <span data-ttu-id="46107-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="46107-132">-SubnetId</span></span>
<span data-ttu-id="46107-133">Sanal ağ alt ağının ARM kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="46107-133">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="46107-134">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="46107-134">-SubscriptionId</span></span>
<span data-ttu-id="46107-135">Bir Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="46107-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="46107-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="46107-136">-Confirm</span></span>
<span data-ttu-id="46107-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="46107-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46107-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46107-138">-WhatIf</span></span>
<span data-ttu-id="46107-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46107-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46107-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="46107-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46107-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46107-141">CommonParameters</span></span>
<span data-ttu-id="46107-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46107-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46107-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="46107-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46107-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46107-144">INPUTS</span></span>

### <span data-ttu-id="46107-145">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Sanarladbıdentity</span><span class="sxs-lookup"><span data-stu-id="46107-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="46107-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46107-146">OUTPUTS</span></span>

### <span data-ttu-id="46107-147">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Api20180601Preview. ıvirtualnetworkrule</span><span class="sxs-lookup"><span data-stu-id="46107-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="46107-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46107-148">NOTES</span></span>

<span data-ttu-id="46107-149">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="46107-149">ALIASES</span></span>

<span data-ttu-id="46107-150">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="46107-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="46107-151">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="46107-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="46107-152">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="46107-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="46107-153">INPUTOBJECT <IMariaDbIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="46107-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="46107-154">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="46107-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="46107-155">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="46107-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="46107-156">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="46107-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="46107-157">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="46107-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="46107-158">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="46107-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="46107-159">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="46107-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="46107-160">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46107-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="46107-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="46107-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="46107-162">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="46107-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="46107-163">`[SubscriptionId <String>]`: Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="46107-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="46107-164">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="46107-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="46107-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46107-165">RELATED LINKS</span></span>

