---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
ms.openlocfilehash: 979fc45bb7bdfe36133404a88a646a871cb33301
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108976"
---
# <span data-ttu-id="8a940-101">Update-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8a940-101">Update-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="8a940-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a940-102">SYNOPSIS</span></span>
<span data-ttu-id="8a940-103">Yeni bir güvenlik duvarı kuralı oluşturur veya varolan bir güvenlik duvarı kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8a940-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="8a940-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a940-104">SYNTAX</span></span>

### <span data-ttu-id="8a940-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8a940-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8a940-106">ClientIpAddress</span><span class="sxs-lookup"><span data-stu-id="8a940-106">ClientIPAddress</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8a940-107">Clientıpaddressviaıdentity</span><span class="sxs-lookup"><span data-stu-id="8a940-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8a940-108">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="8a940-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8a940-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a940-109">DESCRIPTION</span></span>
<span data-ttu-id="8a940-110">Yeni bir güvenlik duvarı kuralı oluşturur veya varolan bir güvenlik duvarı kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8a940-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="8a940-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a940-111">EXAMPLES</span></span>

### <span data-ttu-id="8a940-112">Örnek 1: MySql güvenlik duvarı kuralını adıyla Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="8a940-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="8a940-113">Bu cmdlet, MySql güvenlik duvarı kuralını adıyla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8a940-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="8a940-114">Örnek 2: MySql güvenlik duvarı kuralını kimlik ile güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="8a940-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="8a940-115">Bu cmdlet 'ler, MySql güvenlik duvarı kuralını kimlik ile güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8a940-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

### <span data-ttu-id="8a940-116">Örnek 3: MySql güvenlik duvarı kuralını-ClientIpAddress olarak güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="8a940-116">Example 3: Update MySql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="8a940-117">Bu cmdlet 'ler,</span><span class="sxs-lookup"><span data-stu-id="8a940-117">These cmdlets update MySql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="8a940-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a940-118">PARAMETERS</span></span>

### <span data-ttu-id="8a940-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="8a940-119">-AsJob</span></span>
<span data-ttu-id="8a940-120">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="8a940-120">Run the command as a job</span></span>

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

### <span data-ttu-id="8a940-121">-ClientIpAddress</span><span class="sxs-lookup"><span data-stu-id="8a940-121">-ClientIPAddress</span></span>
<span data-ttu-id="8a940-122">İstemci, sunucu güvenlik duvarı kuralının tek IP belirtti.</span><span class="sxs-lookup"><span data-stu-id="8a940-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="8a940-123">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8a940-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="8a940-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a940-124">-DefaultProfile</span></span>
<span data-ttu-id="8a940-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8a940-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a940-126">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="8a940-126">-EndIPAddress</span></span>
<span data-ttu-id="8a940-127">Sunucu güvenlik duvarı kuralının bitiş IP adresi.</span><span class="sxs-lookup"><span data-stu-id="8a940-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="8a940-128">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8a940-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="8a940-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a940-129">-InputObject</span></span>
<span data-ttu-id="8a940-130">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a940-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a940-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="8a940-131">-Name</span></span>
<span data-ttu-id="8a940-132">Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="8a940-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="8a940-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8a940-133">-NoWait</span></span>
<span data-ttu-id="8a940-134">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="8a940-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8a940-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a940-135">-ResourceGroupName</span></span>
<span data-ttu-id="8a940-136">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8a940-136">The name of the resource group.</span></span>
<span data-ttu-id="8a940-137">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="8a940-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8a940-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8a940-138">-ServerName</span></span>
<span data-ttu-id="8a940-139">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="8a940-139">The name of the server.</span></span>

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

### <span data-ttu-id="8a940-140">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="8a940-140">-StartIPAddress</span></span>
<span data-ttu-id="8a940-141">Sunucu güvenlik duvarı kuralının başlangıç IP adresi.</span><span class="sxs-lookup"><span data-stu-id="8a940-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="8a940-142">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8a940-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="8a940-143">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="8a940-143">-SubscriptionId</span></span>
<span data-ttu-id="8a940-144">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8a940-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8a940-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="8a940-145">-Confirm</span></span>
<span data-ttu-id="8a940-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8a940-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a940-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a940-147">-WhatIf</span></span>
<span data-ttu-id="8a940-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a940-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a940-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8a940-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a940-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a940-150">CommonParameters</span></span>
<span data-ttu-id="8a940-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a940-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a940-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8a940-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a940-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a940-153">INPUTS</span></span>

### <span data-ttu-id="8a940-154">Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Sanysqlidentity</span><span class="sxs-lookup"><span data-stu-id="8a940-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="8a940-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a940-155">OUTPUTS</span></span>

### <span data-ttu-id="8a940-156">Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Api20171201. ıfirewallrule</span><span class="sxs-lookup"><span data-stu-id="8a940-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="8a940-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a940-157">NOTES</span></span>

<span data-ttu-id="8a940-158">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="8a940-158">ALIASES</span></span>

<span data-ttu-id="8a940-159">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="8a940-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8a940-160">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8a940-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a940-161">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8a940-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8a940-162">INPUTOBJECT <IMySqlIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="8a940-162">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8a940-163">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="8a940-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8a940-164">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="8a940-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8a940-165">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="8a940-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8a940-166">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="8a940-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8a940-167">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="8a940-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8a940-168">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8a940-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8a940-169">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="8a940-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="8a940-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="8a940-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8a940-171">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="8a940-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8a940-172">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8a940-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8a940-173">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="8a940-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8a940-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a940-174">RELATED LINKS</span></span>

