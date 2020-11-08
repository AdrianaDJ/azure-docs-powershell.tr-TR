---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: bacd5e1636457fac172cd54c9fcf4407247d88ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265824"
---
# <span data-ttu-id="69c07-101">Remove-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="69c07-101">Remove-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="69c07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69c07-102">SYNOPSIS</span></span>
<span data-ttu-id="69c07-103">Belirtilen ada sahip sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="69c07-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="69c07-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69c07-104">SYNTAX</span></span>

### <span data-ttu-id="69c07-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="69c07-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="69c07-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="69c07-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="69c07-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="69c07-107">DESCRIPTION</span></span>
<span data-ttu-id="69c07-108">Belirtilen ada sahip sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="69c07-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="69c07-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69c07-109">EXAMPLES</span></span>

### <span data-ttu-id="69c07-110">Örnek 1: PostgreSql Server sanal ağ kuralını ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="69c07-110">Example 1: Remove PostgreSql server Virtual Network Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="69c07-111">Bu cmdlet, PostgreSql Server sanal ağ kuralını adıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="69c07-111">This cmdlet removes PostgreSql server Virtual Network Rule by name.</span></span>

### <span data-ttu-id="69c07-112">Örnek 2: http Resql Server sanal ağ kuralını kimlikle kaldırma</span><span class="sxs-lookup"><span data-stu-id="69c07-112">Example 2: Remove PostgreSql server Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -InputObject $ID
 
```

<span data-ttu-id="69c07-113">Bu cmdlet 'ler, https.</span><span class="sxs-lookup"><span data-stu-id="69c07-113">These cmdlets remove PostgreSql server Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="69c07-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69c07-114">PARAMETERS</span></span>

### <span data-ttu-id="69c07-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="69c07-115">-AsJob</span></span>
<span data-ttu-id="69c07-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="69c07-116">Run the command as a job</span></span>

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

### <span data-ttu-id="69c07-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69c07-117">-DefaultProfile</span></span>
<span data-ttu-id="69c07-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="69c07-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69c07-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69c07-119">-InputObject</span></span>
<span data-ttu-id="69c07-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="69c07-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69c07-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="69c07-121">-Name</span></span>
<span data-ttu-id="69c07-122">Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="69c07-122">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69c07-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="69c07-123">-NoWait</span></span>
<span data-ttu-id="69c07-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="69c07-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="69c07-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="69c07-125">-PassThru</span></span>
<span data-ttu-id="69c07-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="69c07-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="69c07-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69c07-127">-ResourceGroupName</span></span>
<span data-ttu-id="69c07-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="69c07-128">The name of the resource group.</span></span>
<span data-ttu-id="69c07-129">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="69c07-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="69c07-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="69c07-130">-ServerName</span></span>
<span data-ttu-id="69c07-131">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="69c07-131">The name of the server.</span></span>

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

### <span data-ttu-id="69c07-132">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="69c07-132">-SubscriptionId</span></span>
<span data-ttu-id="69c07-133">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="69c07-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="69c07-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="69c07-134">-Confirm</span></span>
<span data-ttu-id="69c07-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="69c07-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69c07-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69c07-136">-WhatIf</span></span>
<span data-ttu-id="69c07-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="69c07-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69c07-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="69c07-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69c07-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c07-139">CommonParameters</span></span>
<span data-ttu-id="69c07-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69c07-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c07-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="69c07-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c07-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69c07-142">INPUTS</span></span>

### <span data-ttu-id="69c07-143">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. ıpostgresqlidentity</span><span class="sxs-lookup"><span data-stu-id="69c07-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="69c07-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69c07-144">OUTPUTS</span></span>

### <span data-ttu-id="69c07-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="69c07-145">System.Boolean</span></span>

## <span data-ttu-id="69c07-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69c07-146">NOTES</span></span>

<span data-ttu-id="69c07-147">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="69c07-147">ALIASES</span></span>

<span data-ttu-id="69c07-148">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="69c07-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="69c07-149">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="69c07-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="69c07-150">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="69c07-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="69c07-151">INPUTOBJECT <IPostgreSqlIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="69c07-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="69c07-152">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="69c07-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="69c07-153">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="69c07-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="69c07-154">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="69c07-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="69c07-155">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="69c07-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="69c07-156">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="69c07-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="69c07-157">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="69c07-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="69c07-158">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="69c07-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="69c07-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="69c07-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="69c07-160">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="69c07-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="69c07-161">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="69c07-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="69c07-162">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="69c07-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="69c07-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69c07-163">RELATED LINKS</span></span>

