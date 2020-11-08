---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 43cf2d06c45d545b1d311cea474a8ec69fd49021
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265816"
---
# <span data-ttu-id="6b037-101">Update-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6b037-101">Update-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="6b037-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b037-102">SYNOPSIS</span></span>
<span data-ttu-id="6b037-103">Yeni bir güvenlik duvarı kuralı oluşturur veya varolan bir güvenlik duvarı kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6b037-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="6b037-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b037-104">SYNTAX</span></span>

### <span data-ttu-id="6b037-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6b037-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6b037-106">ClientIpAddress</span><span class="sxs-lookup"><span data-stu-id="6b037-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6b037-107">Clientıpaddressviaıdentity</span><span class="sxs-lookup"><span data-stu-id="6b037-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6b037-108">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="6b037-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="6b037-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b037-109">DESCRIPTION</span></span>
<span data-ttu-id="6b037-110">Yeni bir güvenlik duvarı kuralı oluşturur veya varolan bir güvenlik duvarı kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6b037-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="6b037-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b037-111">EXAMPLES</span></span>

### <span data-ttu-id="6b037-112">Örnek 1: posta kutusu</span><span class="sxs-lookup"><span data-stu-id="6b037-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="6b037-113">Bu cmdlet PostgreSql güvenlik duvarı kuralını adıyla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6b037-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="6b037-114">Örnek 2: posta kodu</span><span class="sxs-lookup"><span data-stu-id="6b037-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="6b037-115">Bu cmdlet 'ler, posta yoluyla PostgreSql güvenlik duvarı kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6b037-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

### <span data-ttu-id="6b037-116">Örnek 3: PostgreSql güvenlik duvarı kuralını-ClientIpAddress olarak güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="6b037-116">Example 3: Update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="6b037-117">Bu cmdlet 'ler, PostgreSql güvenlik duvarı kuralını, tarafından açılır.</span><span class="sxs-lookup"><span data-stu-id="6b037-117">These cmdlets update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="6b037-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b037-118">PARAMETERS</span></span>

### <span data-ttu-id="6b037-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="6b037-119">-AsJob</span></span>
<span data-ttu-id="6b037-120">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="6b037-120">Run the command as a job</span></span>

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

### <span data-ttu-id="6b037-121">-ClientIpAddress</span><span class="sxs-lookup"><span data-stu-id="6b037-121">-ClientIPAddress</span></span>
<span data-ttu-id="6b037-122">İstemci, sunucu güvenlik duvarı kuralının tek IP belirtti.</span><span class="sxs-lookup"><span data-stu-id="6b037-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="6b037-123">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6b037-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6b037-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b037-124">-DefaultProfile</span></span>
<span data-ttu-id="6b037-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6b037-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b037-126">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="6b037-126">-EndIPAddress</span></span>
<span data-ttu-id="6b037-127">Sunucu güvenlik duvarı kuralının bitiş IP adresi.</span><span class="sxs-lookup"><span data-stu-id="6b037-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="6b037-128">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6b037-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6b037-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b037-129">-InputObject</span></span>
<span data-ttu-id="6b037-130">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b037-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b037-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="6b037-131">-Name</span></span>
<span data-ttu-id="6b037-132">Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="6b037-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="6b037-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6b037-133">-NoWait</span></span>
<span data-ttu-id="6b037-134">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="6b037-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6b037-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b037-135">-ResourceGroupName</span></span>
<span data-ttu-id="6b037-136">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6b037-136">The name of the resource group.</span></span>
<span data-ttu-id="6b037-137">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="6b037-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6b037-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6b037-138">-ServerName</span></span>
<span data-ttu-id="6b037-139">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="6b037-139">The name of the server.</span></span>

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

### <span data-ttu-id="6b037-140">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="6b037-140">-StartIPAddress</span></span>
<span data-ttu-id="6b037-141">Sunucu güvenlik duvarı kuralının başlangıç IP adresi.</span><span class="sxs-lookup"><span data-stu-id="6b037-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="6b037-142">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6b037-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6b037-143">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="6b037-143">-SubscriptionId</span></span>
<span data-ttu-id="6b037-144">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6b037-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6b037-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="6b037-145">-Confirm</span></span>
<span data-ttu-id="6b037-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6b037-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b037-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b037-147">-WhatIf</span></span>
<span data-ttu-id="6b037-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b037-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b037-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6b037-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b037-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b037-150">CommonParameters</span></span>
<span data-ttu-id="6b037-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b037-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b037-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6b037-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b037-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b037-153">INPUTS</span></span>

### <span data-ttu-id="6b037-154">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. ıpostgresqlidentity</span><span class="sxs-lookup"><span data-stu-id="6b037-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="6b037-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b037-155">OUTPUTS</span></span>

### <span data-ttu-id="6b037-156">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. Api20171201. ıfirewallrule</span><span class="sxs-lookup"><span data-stu-id="6b037-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="6b037-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b037-157">NOTES</span></span>

<span data-ttu-id="6b037-158">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="6b037-158">ALIASES</span></span>

<span data-ttu-id="6b037-159">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="6b037-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6b037-160">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6b037-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b037-161">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6b037-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6b037-162">INPUTOBJECT <IPostgreSqlIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="6b037-162">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6b037-163">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="6b037-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6b037-164">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="6b037-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6b037-165">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="6b037-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6b037-166">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="6b037-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6b037-167">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="6b037-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6b037-168">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6b037-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6b037-169">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="6b037-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="6b037-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="6b037-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6b037-171">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="6b037-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6b037-172">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6b037-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6b037-173">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="6b037-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6b037-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b037-174">RELATED LINKS</span></span>

