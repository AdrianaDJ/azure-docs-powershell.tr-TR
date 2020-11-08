---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
ms.openlocfilehash: 11278c1d317f6f4e0171513a4503c5681506f1ac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278595"
---
# <span data-ttu-id="0b4bf-101">Get-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0b4bf-101">Get-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="0b4bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b4bf-102">SYNOPSIS</span></span>
<span data-ttu-id="0b4bf-103">Sunucu güvenlik duvarı kuralı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="0b4bf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b4bf-104">SYNTAX</span></span>

### <span data-ttu-id="0b4bf-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0b4bf-105">List (Default)</span></span>
```
Get-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0b4bf-106">Al</span><span class="sxs-lookup"><span data-stu-id="0b4bf-106">Get</span></span>
```
Get-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0b4bf-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="0b4bf-107">GetViaIdentity</span></span>
```
Get-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0b4bf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b4bf-108">DESCRIPTION</span></span>
<span data-ttu-id="0b4bf-109">Sunucu güvenlik duvarı kuralı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="0b4bf-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b4bf-110">EXAMPLES</span></span>

### <span data-ttu-id="0b4bf-111">Örnek 1: belirtilen MySql sunucusundaki tüm güvenlik duvarı kurallarını listeler</span><span class="sxs-lookup"><span data-stu-id="0b4bf-111">Example 1: Lists all the Firewall Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="0b4bf-112">Bu cmdlet, belirtilen MySql sunucusundaki tüm güvenlik duvarı kuralını listeler.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-112">This cmdlet lists all the Firewall Rule in specified MySql server.</span></span>

### <span data-ttu-id="0b4bf-113">Örnek 2: ada göre güvenlik duvarı kuralı alma</span><span class="sxs-lookup"><span data-stu-id="0b4bf-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="0b4bf-114">Bu cmdlet güvenlik duvarının kuralını adıyla alır.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="0b4bf-115">Örnek 3: kimlikte güvenlik duvarı kuralı alma</span><span class="sxs-lookup"><span data-stu-id="0b4bf-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Get-AzMySqlFirewallRule -InputObject $ID

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="0b4bf-116">Bu cmdlet güvenlik duvarının kuralını kimliğe getirir.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="0b4bf-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b4bf-117">PARAMETERS</span></span>

### <span data-ttu-id="0b4bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b4bf-118">-DefaultProfile</span></span>
<span data-ttu-id="0b4bf-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b4bf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b4bf-120">-InputObject</span></span>
<span data-ttu-id="0b4bf-121">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b4bf-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="0b4bf-122">-Name</span></span>
<span data-ttu-id="0b4bf-123">Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="0b4bf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b4bf-124">-ResourceGroupName</span></span>
<span data-ttu-id="0b4bf-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-125">The name of the resource group.</span></span>
<span data-ttu-id="0b4bf-126">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0b4bf-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0b4bf-127">-ServerName</span></span>
<span data-ttu-id="0b4bf-128">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-128">The name of the server.</span></span>

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

### <span data-ttu-id="0b4bf-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="0b4bf-129">-SubscriptionId</span></span>
<span data-ttu-id="0b4bf-130">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0b4bf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b4bf-131">CommonParameters</span></span>
<span data-ttu-id="0b4bf-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b4bf-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b4bf-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b4bf-134">INPUTS</span></span>

### <span data-ttu-id="0b4bf-135">Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Sanysqlidentity</span><span class="sxs-lookup"><span data-stu-id="0b4bf-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="0b4bf-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b4bf-136">OUTPUTS</span></span>

### <span data-ttu-id="0b4bf-137">Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Api20171201. ıfirewallrule</span><span class="sxs-lookup"><span data-stu-id="0b4bf-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="0b4bf-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b4bf-138">NOTES</span></span>

<span data-ttu-id="0b4bf-139">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="0b4bf-139">ALIASES</span></span>

<span data-ttu-id="0b4bf-140">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="0b4bf-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0b4bf-141">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0b4bf-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0b4bf-143">INPUTOBJECT <IMySqlIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="0b4bf-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0b4bf-144">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0b4bf-145">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0b4bf-146">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0b4bf-147">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="0b4bf-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0b4bf-148">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0b4bf-149">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0b4bf-150">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="0b4bf-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0b4bf-152">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0b4bf-153">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0b4bf-154">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0b4bf-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b4bf-155">RELATED LINKS</span></span>

