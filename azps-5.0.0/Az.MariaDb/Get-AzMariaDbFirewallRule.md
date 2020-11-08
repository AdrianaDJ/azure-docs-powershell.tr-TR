---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
ms.openlocfilehash: 2b2f52d8dc4f9e31a86b666b7ee81981fa6bd18c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278909"
---
# <span data-ttu-id="1de03-101">Get-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1de03-101">Get-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="1de03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1de03-102">SYNOPSIS</span></span>
<span data-ttu-id="1de03-103">Sunucu güvenlik duvarı kuralı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="1de03-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="1de03-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1de03-104">SYNTAX</span></span>

### <span data-ttu-id="1de03-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1de03-105">List (Default)</span></span>
```
Get-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1de03-106">Al</span><span class="sxs-lookup"><span data-stu-id="1de03-106">Get</span></span>
```
Get-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1de03-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="1de03-107">GetViaIdentity</span></span>
```
Get-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1de03-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1de03-108">DESCRIPTION</span></span>
<span data-ttu-id="1de03-109">Sunucu güvenlik duvarı kuralı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="1de03-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="1de03-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1de03-110">EXAMPLES</span></span>

### <span data-ttu-id="1de03-111">Örnek 1: bir Mari</span><span class="sxs-lookup"><span data-stu-id="1de03-111">Example 1: List all firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

Name       Type
----       ----
fr-cfgl3y  Microsoft.DBforMariaDB/servers/firewallRules
fr-usc9na  Microsoft.DBforMariaDB/servers/firewallRules
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="1de03-112">Bu komut, bir MariaDB 'ın altındaki tüm girewall kuralını listeler.</span><span class="sxs-lookup"><span data-stu-id="1de03-112">This command lists all girewall rule under a MariaDB.</span></span>

### <span data-ttu-id="1de03-113">Örnek 2: bir Mari</span><span class="sxs-lookup"><span data-stu-id="1de03-113">Example 2: Get a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig -Name frname-001

Name       Type
----       ----
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="1de03-114">Bu komut bir MariaDB altında bir güvenlik duvarı kuralı alır.</span><span class="sxs-lookup"><span data-stu-id="1de03-114">This command gets a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="1de03-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1de03-115">PARAMETERS</span></span>

### <span data-ttu-id="1de03-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1de03-116">-DefaultProfile</span></span>
<span data-ttu-id="1de03-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1de03-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1de03-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1de03-118">-InputObject</span></span>
<span data-ttu-id="1de03-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1de03-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1de03-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="1de03-120">-Name</span></span>
<span data-ttu-id="1de03-121">Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="1de03-121">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de03-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1de03-122">-ResourceGroupName</span></span>
<span data-ttu-id="1de03-123">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1de03-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="1de03-124">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1de03-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de03-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1de03-125">-ServerName</span></span>
<span data-ttu-id="1de03-126">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="1de03-126">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de03-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="1de03-127">-SubscriptionId</span></span>
<span data-ttu-id="1de03-128">Bir Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1de03-128">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de03-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1de03-129">CommonParameters</span></span>
<span data-ttu-id="1de03-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1de03-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1de03-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1de03-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1de03-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1de03-132">INPUTS</span></span>

### <span data-ttu-id="1de03-133">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Sanarladbıdentity</span><span class="sxs-lookup"><span data-stu-id="1de03-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="1de03-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1de03-134">OUTPUTS</span></span>

### <span data-ttu-id="1de03-135">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Api20180601Preview. ıfirewallrule</span><span class="sxs-lookup"><span data-stu-id="1de03-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="1de03-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1de03-136">NOTES</span></span>

<span data-ttu-id="1de03-137">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="1de03-137">ALIASES</span></span>

<span data-ttu-id="1de03-138">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="1de03-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1de03-139">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1de03-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1de03-140">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1de03-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1de03-141">INPUTOBJECT <IMariaDbIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="1de03-141">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1de03-142">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="1de03-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="1de03-143">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="1de03-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="1de03-144">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="1de03-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="1de03-145">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="1de03-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1de03-146">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="1de03-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="1de03-147">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1de03-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="1de03-148">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1de03-148">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="1de03-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="1de03-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="1de03-150">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="1de03-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="1de03-151">`[SubscriptionId <String>]`: Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1de03-151">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="1de03-152">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="1de03-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="1de03-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1de03-153">RELATED LINKS</span></span>

