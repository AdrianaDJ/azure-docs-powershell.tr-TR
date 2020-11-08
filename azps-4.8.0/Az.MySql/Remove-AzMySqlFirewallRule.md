---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFirewallRule.md
ms.openlocfilehash: 1036fb17cb83e28a76e4765b5fc64d703c2e014b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267260"
---
# <span data-ttu-id="5a3d7-101">Remove-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5a3d7-101">Remove-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="5a3d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a3d7-102">SYNOPSIS</span></span>
<span data-ttu-id="5a3d7-103">Sunucu güvenlik duvarı kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="5a3d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a3d7-104">SYNTAX</span></span>

### <span data-ttu-id="5a3d7-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5a3d7-105">Delete (Default)</span></span>
```
Remove-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5a3d7-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="5a3d7-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5a3d7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a3d7-107">DESCRIPTION</span></span>
<span data-ttu-id="5a3d7-108">Sunucu güvenlik duvarı kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="5a3d7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a3d7-109">EXAMPLES</span></span>

### <span data-ttu-id="5a3d7-110">Örnek 1: MySql güvenlik duvarı kuralını adla kaldırma</span><span class="sxs-lookup"><span data-stu-id="5a3d7-110">Example 1: Remove MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

```

<span data-ttu-id="5a3d7-111">Bu cmdlet MySql güvenlik duvarı kuralını adıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-111">This cmdlet removes MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="5a3d7-112">Örnek 2: MySql güvenlik duvarı kuralını kimlikle kaldırma</span><span class="sxs-lookup"><span data-stu-id="5a3d7-112">Example 2: Remove MySql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Remove-AzMySqlFirewallRule -InputObject $ID
 
```

<span data-ttu-id="5a3d7-113">Bu cmdlet 'ler, MySql güvenlik duvarı kuralını kimlik ile kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-113">These cmdlets remove MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="5a3d7-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a3d7-114">PARAMETERS</span></span>

### <span data-ttu-id="5a3d7-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="5a3d7-115">-AsJob</span></span>
<span data-ttu-id="5a3d7-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="5a3d7-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5a3d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a3d7-117">-DefaultProfile</span></span>
<span data-ttu-id="5a3d7-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a3d7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a3d7-119">-InputObject</span></span>
<span data-ttu-id="5a3d7-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a3d7-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="5a3d7-121">-Name</span></span>
<span data-ttu-id="5a3d7-122">Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-122">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a3d7-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5a3d7-123">-NoWait</span></span>
<span data-ttu-id="5a3d7-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="5a3d7-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5a3d7-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5a3d7-125">-PassThru</span></span>
<span data-ttu-id="5a3d7-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="5a3d7-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5a3d7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a3d7-127">-ResourceGroupName</span></span>
<span data-ttu-id="5a3d7-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-128">The name of the resource group.</span></span>
<span data-ttu-id="5a3d7-129">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a3d7-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5a3d7-130">-ServerName</span></span>
<span data-ttu-id="5a3d7-131">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a3d7-132">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="5a3d7-132">-SubscriptionId</span></span>
<span data-ttu-id="5a3d7-133">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a3d7-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="5a3d7-134">-Confirm</span></span>
<span data-ttu-id="5a3d7-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a3d7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a3d7-136">-WhatIf</span></span>
<span data-ttu-id="5a3d7-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a3d7-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a3d7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a3d7-139">CommonParameters</span></span>
<span data-ttu-id="5a3d7-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a3d7-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a3d7-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a3d7-142">INPUTS</span></span>

### <span data-ttu-id="5a3d7-143">Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Sanysqlidentity</span><span class="sxs-lookup"><span data-stu-id="5a3d7-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="5a3d7-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a3d7-144">OUTPUTS</span></span>

### <span data-ttu-id="5a3d7-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5a3d7-145">System.Boolean</span></span>

## <span data-ttu-id="5a3d7-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a3d7-146">NOTES</span></span>

<span data-ttu-id="5a3d7-147">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="5a3d7-147">ALIASES</span></span>

<span data-ttu-id="5a3d7-148">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="5a3d7-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5a3d7-149">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5a3d7-150">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5a3d7-151">INPUTOBJECT <IMySqlIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="5a3d7-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5a3d7-152">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="5a3d7-153">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="5a3d7-154">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="5a3d7-155">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="5a3d7-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5a3d7-156">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="5a3d7-157">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5a3d7-158">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="5a3d7-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="5a3d7-160">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="5a3d7-161">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5a3d7-162">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="5a3d7-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="5a3d7-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a3d7-163">RELATED LINKS</span></span>

