---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7d474000ed8c449c95ae7319a960c5f748d80e66
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267105"
---
# <span data-ttu-id="65d33-101">Update-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="65d33-101">Update-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="65d33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65d33-102">SYNOPSIS</span></span>
<span data-ttu-id="65d33-103">Yeni bir güvenlik duvarı kuralı oluşturur veya varolan bir güvenlik duvarı kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="65d33-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="65d33-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65d33-104">SYNTAX</span></span>

### <span data-ttu-id="65d33-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="65d33-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="65d33-106">ClientIpAddress</span><span class="sxs-lookup"><span data-stu-id="65d33-106">ClientIPAddress</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="65d33-107">Clientıpaddressviaıdentity</span><span class="sxs-lookup"><span data-stu-id="65d33-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="65d33-108">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="65d33-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="65d33-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="65d33-109">DESCRIPTION</span></span>
<span data-ttu-id="65d33-110">Yeni bir güvenlik duvarı kuralı oluşturur veya varolan bir güvenlik duvarı kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="65d33-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="65d33-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65d33-111">EXAMPLES</span></span>

### <span data-ttu-id="65d33-112">Örnek 1: MariaDB güvenlik duvarı kuralını Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="65d33-112">Example 1: Update MariaDB firewall rule</span></span>
```powershell
PS C:\> Update-AzMariaDbFirewallRule -Name fr-cfgl3y -ServerName mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StartIPAddress 0.0.3.1 -EndIPAddress 0.0.3.255

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.3.1        0.0.3.255
```

<span data-ttu-id="65d33-113">Bu komut bir MariaDB güvenlik duvarı kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="65d33-113">This command updates a MariaDB firewall rule.</span></span>

### <span data-ttu-id="65d33-114">Örnek 2: MariaDB güvenlik duvarı kuralını Identity olarak güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="65d33-114">Example 2: Update MariaDB Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.3
```

<span data-ttu-id="65d33-115">Cmdlet, MariaDB güvenlik duvarı kuralını kimlik olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="65d33-115">The cmdlet updates MariaDB Firewall Rule by identity.</span></span>

### <span data-ttu-id="65d33-116">Örnek 3: MariaDB güvenlik duvarı kuralını-ClientIpAddress.</span><span class="sxs-lookup"><span data-stu-id="65d33-116">Example 3: Update MariaDB Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.2
```

<span data-ttu-id="65d33-117">Cmdlet, MariaDB güvenlik duvarının gönderdiği Mariaddress.</span><span class="sxs-lookup"><span data-stu-id="65d33-117">The cmdlet updates MariaDB Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="65d33-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65d33-118">PARAMETERS</span></span>

### <span data-ttu-id="65d33-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="65d33-119">-AsJob</span></span>
<span data-ttu-id="65d33-120">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="65d33-120">Run the command as a job</span></span>

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

### <span data-ttu-id="65d33-121">-ClientIpAddress</span><span class="sxs-lookup"><span data-stu-id="65d33-121">-ClientIPAddress</span></span>
<span data-ttu-id="65d33-122">İstemci, sunucu güvenlik duvarı kuralının tek IP belirtti.</span><span class="sxs-lookup"><span data-stu-id="65d33-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="65d33-123">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="65d33-123">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, ClientIPAddressViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d33-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d33-124">-DefaultProfile</span></span>
<span data-ttu-id="65d33-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="65d33-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65d33-126">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="65d33-126">-EndIPAddress</span></span>
<span data-ttu-id="65d33-127">Sunucu güvenlik duvarı kuralının bitiş IP adresi.</span><span class="sxs-lookup"><span data-stu-id="65d33-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="65d33-128">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="65d33-128">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d33-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65d33-129">-InputObject</span></span>
<span data-ttu-id="65d33-130">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="65d33-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65d33-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="65d33-131">-Name</span></span>
<span data-ttu-id="65d33-132">Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="65d33-132">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d33-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="65d33-133">-NoWait</span></span>
<span data-ttu-id="65d33-134">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="65d33-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="65d33-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65d33-135">-ResourceGroupName</span></span>
<span data-ttu-id="65d33-136">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="65d33-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="65d33-137">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65d33-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d33-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="65d33-138">-ServerName</span></span>
<span data-ttu-id="65d33-139">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="65d33-139">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d33-140">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="65d33-140">-StartIPAddress</span></span>
<span data-ttu-id="65d33-141">Sunucu güvenlik duvarı kuralının başlangıç IP adresi.</span><span class="sxs-lookup"><span data-stu-id="65d33-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="65d33-142">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="65d33-142">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d33-143">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="65d33-143">-SubscriptionId</span></span>
<span data-ttu-id="65d33-144">Bir Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="65d33-144">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d33-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="65d33-145">-Confirm</span></span>
<span data-ttu-id="65d33-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="65d33-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65d33-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65d33-147">-WhatIf</span></span>
<span data-ttu-id="65d33-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="65d33-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65d33-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="65d33-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65d33-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d33-150">CommonParameters</span></span>
<span data-ttu-id="65d33-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65d33-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d33-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="65d33-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d33-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65d33-153">INPUTS</span></span>

### <span data-ttu-id="65d33-154">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Sanarladbıdentity</span><span class="sxs-lookup"><span data-stu-id="65d33-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="65d33-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65d33-155">OUTPUTS</span></span>

### <span data-ttu-id="65d33-156">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Api20180601Preview. ıfirewallrule</span><span class="sxs-lookup"><span data-stu-id="65d33-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="65d33-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65d33-157">NOTES</span></span>

<span data-ttu-id="65d33-158">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="65d33-158">ALIASES</span></span>

<span data-ttu-id="65d33-159">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="65d33-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="65d33-160">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="65d33-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="65d33-161">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="65d33-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="65d33-162">INPUTOBJECT <IMariaDbIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="65d33-162">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="65d33-163">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="65d33-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="65d33-164">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="65d33-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="65d33-165">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="65d33-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="65d33-166">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="65d33-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="65d33-167">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="65d33-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="65d33-168">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="65d33-168">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="65d33-169">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65d33-169">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="65d33-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="65d33-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="65d33-171">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="65d33-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="65d33-172">`[SubscriptionId <String>]`: Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="65d33-172">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="65d33-173">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="65d33-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="65d33-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65d33-174">RELATED LINKS</span></span>

