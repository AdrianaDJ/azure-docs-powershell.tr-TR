---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 85690d3602744f6bde45a5f08b5a927124a8460a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108168"
---
# <span data-ttu-id="bbedf-101">Remove-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bbedf-101">Remove-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="bbedf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbedf-102">SYNOPSIS</span></span>
<span data-ttu-id="bbedf-103">Belirtilen ada sahip sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="bbedf-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="bbedf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bbedf-104">SYNTAX</span></span>

### <span data-ttu-id="bbedf-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bbedf-105">Delete (Default)</span></span>
```
Remove-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="bbedf-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="bbedf-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bbedf-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bbedf-107">DESCRIPTION</span></span>
<span data-ttu-id="bbedf-108">Belirtilen ada sahip sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="bbedf-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="bbedf-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bbedf-109">EXAMPLES</span></span>

### <span data-ttu-id="bbedf-110">Örnek 1: MySql Server sanal ağ kuralını ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="bbedf-110">Example 1: Remove MySql server Virtual Network Rule by name</span></span>
```powershell
PS C:\> Remove-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest-ServerName mysql-test

```

<span data-ttu-id="bbedf-111">Bu cmdlet MySql sunucusu sanal ağ kuralını adıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bbedf-111">This cmdlet removes MySql server Virtual Network Rule by name.</span></span>

### <span data-ttu-id="bbedf-112">Örnek 2: MySql Server sanal ağ kuralını kimliğe göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="bbedf-112">Example 2: Remove MySql server Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Remove-AzMySqlVirtualNetworkRule -InputObject $ID
 
```

<span data-ttu-id="bbedf-113">Bu cmdlet 'ler MySql sunucusu sanal ağ kuralını kimliğe göre kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bbedf-113">These cmdlets remove MySql server Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="bbedf-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bbedf-114">PARAMETERS</span></span>

### <span data-ttu-id="bbedf-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="bbedf-115">-AsJob</span></span>
<span data-ttu-id="bbedf-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="bbedf-116">Run the command as a job</span></span>

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

### <span data-ttu-id="bbedf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbedf-117">-DefaultProfile</span></span>
<span data-ttu-id="bbedf-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bbedf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbedf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbedf-119">-InputObject</span></span>
<span data-ttu-id="bbedf-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bbedf-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bbedf-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="bbedf-121">-Name</span></span>
<span data-ttu-id="bbedf-122">Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="bbedf-122">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="bbedf-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bbedf-123">-NoWait</span></span>
<span data-ttu-id="bbedf-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="bbedf-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bbedf-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bbedf-125">-PassThru</span></span>
<span data-ttu-id="bbedf-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="bbedf-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bbedf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbedf-127">-ResourceGroupName</span></span>
<span data-ttu-id="bbedf-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bbedf-128">The name of the resource group.</span></span>
<span data-ttu-id="bbedf-129">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="bbedf-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bbedf-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bbedf-130">-ServerName</span></span>
<span data-ttu-id="bbedf-131">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="bbedf-131">The name of the server.</span></span>

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

### <span data-ttu-id="bbedf-132">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="bbedf-132">-SubscriptionId</span></span>
<span data-ttu-id="bbedf-133">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bbedf-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bbedf-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="bbedf-134">-Confirm</span></span>
<span data-ttu-id="bbedf-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bbedf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbedf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbedf-136">-WhatIf</span></span>
<span data-ttu-id="bbedf-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bbedf-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbedf-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bbedf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbedf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbedf-139">CommonParameters</span></span>
<span data-ttu-id="bbedf-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bbedf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbedf-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bbedf-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbedf-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bbedf-142">INPUTS</span></span>

### <span data-ttu-id="bbedf-143">Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Sanysqlidentity</span><span class="sxs-lookup"><span data-stu-id="bbedf-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="bbedf-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bbedf-144">OUTPUTS</span></span>

### <span data-ttu-id="bbedf-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bbedf-145">System.Boolean</span></span>

## <span data-ttu-id="bbedf-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bbedf-146">NOTES</span></span>

<span data-ttu-id="bbedf-147">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="bbedf-147">ALIASES</span></span>

<span data-ttu-id="bbedf-148">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="bbedf-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bbedf-149">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bbedf-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bbedf-150">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bbedf-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bbedf-151">INPUTOBJECT <IMySqlIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="bbedf-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bbedf-152">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="bbedf-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="bbedf-153">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="bbedf-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="bbedf-154">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="bbedf-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="bbedf-155">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="bbedf-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bbedf-156">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="bbedf-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="bbedf-157">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bbedf-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bbedf-158">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="bbedf-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="bbedf-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="bbedf-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="bbedf-160">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="bbedf-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="bbedf-161">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bbedf-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bbedf-162">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="bbedf-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="bbedf-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bbedf-163">RELATED LINKS</span></span>

