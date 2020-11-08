---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7775c4adeef0ce4b05efa2b54c6484408256f3eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278641"
---
# <span data-ttu-id="d5893-101">Remove-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d5893-101">Remove-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="d5893-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5893-102">SYNOPSIS</span></span>
<span data-ttu-id="d5893-103">Sunucu güvenlik duvarı kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="d5893-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="d5893-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5893-104">SYNTAX</span></span>

### <span data-ttu-id="d5893-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d5893-105">Delete (Default)</span></span>
```
Remove-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d5893-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="d5893-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d5893-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5893-107">DESCRIPTION</span></span>
<span data-ttu-id="d5893-108">Sunucu güvenlik duvarı kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="d5893-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="d5893-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5893-109">EXAMPLES</span></span>

### <span data-ttu-id="d5893-110">Örnek 1: bir Mari</span><span class="sxs-lookup"><span data-stu-id="d5893-110">Example 1: Remove a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Remove-AzMariaDbFirewallRule -Name frname-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

```

<span data-ttu-id="d5893-111">Bu komut bir MariaDB altında bir güvenlik duvarı kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d5893-111">This command removes a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="d5893-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5893-112">PARAMETERS</span></span>

### <span data-ttu-id="d5893-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="d5893-113">-AsJob</span></span>
<span data-ttu-id="d5893-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="d5893-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d5893-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5893-115">-DefaultProfile</span></span>
<span data-ttu-id="d5893-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d5893-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5893-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5893-117">-InputObject</span></span>
<span data-ttu-id="d5893-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d5893-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5893-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d5893-119">-Name</span></span>
<span data-ttu-id="d5893-120">Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="d5893-120">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="d5893-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d5893-121">-NoWait</span></span>
<span data-ttu-id="d5893-122">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="d5893-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d5893-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d5893-123">-PassThru</span></span>
<span data-ttu-id="d5893-124">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="d5893-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d5893-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5893-125">-ResourceGroupName</span></span>
<span data-ttu-id="d5893-126">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d5893-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d5893-127">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d5893-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d5893-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d5893-128">-ServerName</span></span>
<span data-ttu-id="d5893-129">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="d5893-129">The name of the server.</span></span>

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

### <span data-ttu-id="d5893-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d5893-130">-SubscriptionId</span></span>
<span data-ttu-id="d5893-131">Bir Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d5893-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="d5893-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="d5893-132">-Confirm</span></span>
<span data-ttu-id="d5893-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d5893-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5893-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5893-134">-WhatIf</span></span>
<span data-ttu-id="d5893-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d5893-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5893-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d5893-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5893-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5893-137">CommonParameters</span></span>
<span data-ttu-id="d5893-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5893-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5893-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d5893-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5893-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5893-140">INPUTS</span></span>

### <span data-ttu-id="d5893-141">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Sanarladbıdentity</span><span class="sxs-lookup"><span data-stu-id="d5893-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="d5893-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5893-142">OUTPUTS</span></span>

### <span data-ttu-id="d5893-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d5893-143">System.Boolean</span></span>

## <span data-ttu-id="d5893-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5893-144">NOTES</span></span>

<span data-ttu-id="d5893-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="d5893-145">ALIASES</span></span>

<span data-ttu-id="d5893-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="d5893-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d5893-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d5893-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d5893-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d5893-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d5893-149">INPUTOBJECT <IMariaDbIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="d5893-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d5893-150">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="d5893-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d5893-151">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="d5893-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d5893-152">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="d5893-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d5893-153">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="d5893-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d5893-154">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="d5893-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d5893-155">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d5893-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d5893-156">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d5893-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d5893-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="d5893-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d5893-158">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="d5893-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d5893-159">`[SubscriptionId <String>]`: Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d5893-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="d5893-160">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="d5893-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d5893-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5893-161">RELATED LINKS</span></span>

