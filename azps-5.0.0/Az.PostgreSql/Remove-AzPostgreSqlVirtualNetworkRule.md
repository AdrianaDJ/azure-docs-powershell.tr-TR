---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: bacd5e1636457fac172cd54c9fcf4407247d88ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277566"
---
# <span data-ttu-id="fea48-101">Remove-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fea48-101">Remove-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="fea48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fea48-102">SYNOPSIS</span></span>
<span data-ttu-id="fea48-103">Belirtilen ada sahip sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="fea48-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="fea48-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fea48-104">SYNTAX</span></span>

### <span data-ttu-id="fea48-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fea48-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="fea48-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="fea48-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fea48-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fea48-107">DESCRIPTION</span></span>
<span data-ttu-id="fea48-108">Belirtilen ada sahip sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="fea48-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="fea48-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fea48-109">EXAMPLES</span></span>

### <span data-ttu-id="fea48-110">Örnek 1: PostgreSql Server sanal ağ kuralını ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="fea48-110">Example 1: Remove PostgreSql server Virtual Network Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="fea48-111">Bu cmdlet, PostgreSql Server sanal ağ kuralını adıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fea48-111">This cmdlet removes PostgreSql server Virtual Network Rule by name.</span></span>

### <span data-ttu-id="fea48-112">Örnek 2: http Resql Server sanal ağ kuralını kimlikle kaldırma</span><span class="sxs-lookup"><span data-stu-id="fea48-112">Example 2: Remove PostgreSql server Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -InputObject $ID
 
```

<span data-ttu-id="fea48-113">Bu cmdlet 'ler, https.</span><span class="sxs-lookup"><span data-stu-id="fea48-113">These cmdlets remove PostgreSql server Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="fea48-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fea48-114">PARAMETERS</span></span>

### <span data-ttu-id="fea48-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="fea48-115">-AsJob</span></span>
<span data-ttu-id="fea48-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="fea48-116">Run the command as a job</span></span>

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

### <span data-ttu-id="fea48-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fea48-117">-DefaultProfile</span></span>
<span data-ttu-id="fea48-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fea48-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fea48-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fea48-119">-InputObject</span></span>
<span data-ttu-id="fea48-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fea48-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fea48-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="fea48-121">-Name</span></span>
<span data-ttu-id="fea48-122">Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="fea48-122">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="fea48-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fea48-123">-NoWait</span></span>
<span data-ttu-id="fea48-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="fea48-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fea48-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fea48-125">-PassThru</span></span>
<span data-ttu-id="fea48-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="fea48-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fea48-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fea48-127">-ResourceGroupName</span></span>
<span data-ttu-id="fea48-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fea48-128">The name of the resource group.</span></span>
<span data-ttu-id="fea48-129">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="fea48-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fea48-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fea48-130">-ServerName</span></span>
<span data-ttu-id="fea48-131">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="fea48-131">The name of the server.</span></span>

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

### <span data-ttu-id="fea48-132">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="fea48-132">-SubscriptionId</span></span>
<span data-ttu-id="fea48-133">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="fea48-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fea48-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="fea48-134">-Confirm</span></span>
<span data-ttu-id="fea48-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fea48-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fea48-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fea48-136">-WhatIf</span></span>
<span data-ttu-id="fea48-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fea48-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fea48-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fea48-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fea48-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea48-139">CommonParameters</span></span>
<span data-ttu-id="fea48-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fea48-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea48-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fea48-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea48-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fea48-142">INPUTS</span></span>

### <span data-ttu-id="fea48-143">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. ıpostgresqlidentity</span><span class="sxs-lookup"><span data-stu-id="fea48-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="fea48-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fea48-144">OUTPUTS</span></span>

### <span data-ttu-id="fea48-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fea48-145">System.Boolean</span></span>

## <span data-ttu-id="fea48-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fea48-146">NOTES</span></span>

<span data-ttu-id="fea48-147">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="fea48-147">ALIASES</span></span>

<span data-ttu-id="fea48-148">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="fea48-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fea48-149">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="fea48-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fea48-150">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fea48-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fea48-151">INPUTOBJECT <IPostgreSqlIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="fea48-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fea48-152">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="fea48-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="fea48-153">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="fea48-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="fea48-154">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="fea48-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="fea48-155">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="fea48-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fea48-156">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="fea48-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="fea48-157">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fea48-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fea48-158">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="fea48-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="fea48-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="fea48-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="fea48-160">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="fea48-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="fea48-161">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="fea48-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fea48-162">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="fea48-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="fea48-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fea48-163">RELATED LINKS</span></span>

