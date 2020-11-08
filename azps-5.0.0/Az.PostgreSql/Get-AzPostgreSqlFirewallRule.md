---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: a5691b1d8181d210770802c8d3aa4526b6bd72f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278226"
---
# <span data-ttu-id="60c92-101">Get-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="60c92-101">Get-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="60c92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60c92-102">SYNOPSIS</span></span>
<span data-ttu-id="60c92-103">Sunucu güvenlik duvarı kuralı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="60c92-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="60c92-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="60c92-104">SYNTAX</span></span>

### <span data-ttu-id="60c92-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="60c92-105">List (Default)</span></span>
```
Get-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="60c92-106">Al</span><span class="sxs-lookup"><span data-stu-id="60c92-106">Get</span></span>
```
Get-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="60c92-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="60c92-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="60c92-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="60c92-108">DESCRIPTION</span></span>
<span data-ttu-id="60c92-109">Sunucu güvenlik duvarı kuralı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="60c92-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="60c92-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="60c92-110">EXAMPLES</span></span>

### <span data-ttu-id="60c92-111">Örnek 1: belirtilen PostgreSql sunucusundaki tüm güvenlik duvarı kurallarını listeler</span><span class="sxs-lookup"><span data-stu-id="60c92-111">Example 1: Lists all the Firewall Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="60c92-112">Bu cmdlet, belirtilen PostgreSql sunucusundaki tüm güvenlik duvarı kuralını listeler.</span><span class="sxs-lookup"><span data-stu-id="60c92-112">This cmdlet lists all the Firewall Rule in specified PostgreSql server.</span></span>

### <span data-ttu-id="60c92-113">Örnek 2: ada göre güvenlik duvarı kuralı alma</span><span class="sxs-lookup"><span data-stu-id="60c92-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="60c92-114">Bu cmdlet güvenlik duvarının kuralını adıyla alır.</span><span class="sxs-lookup"><span data-stu-id="60c92-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="60c92-115">Örnek 3: kimlikte güvenlik duvarı kuralı alma</span><span class="sxs-lookup"><span data-stu-id="60c92-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Get-AzPostgreSqlFirewallRule -InputObject $ID

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="60c92-116">Bu cmdlet güvenlik duvarının kuralını kimliğe getirir.</span><span class="sxs-lookup"><span data-stu-id="60c92-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="60c92-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="60c92-117">PARAMETERS</span></span>

### <span data-ttu-id="60c92-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60c92-118">-DefaultProfile</span></span>
<span data-ttu-id="60c92-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="60c92-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60c92-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60c92-120">-InputObject</span></span>
<span data-ttu-id="60c92-121">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="60c92-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60c92-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="60c92-122">-Name</span></span>
<span data-ttu-id="60c92-123">Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="60c92-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="60c92-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60c92-124">-ResourceGroupName</span></span>
<span data-ttu-id="60c92-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="60c92-125">The name of the resource group.</span></span>
<span data-ttu-id="60c92-126">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="60c92-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="60c92-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="60c92-127">-ServerName</span></span>
<span data-ttu-id="60c92-128">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="60c92-128">The name of the server.</span></span>

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

### <span data-ttu-id="60c92-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="60c92-129">-SubscriptionId</span></span>
<span data-ttu-id="60c92-130">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="60c92-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="60c92-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60c92-131">CommonParameters</span></span>
<span data-ttu-id="60c92-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="60c92-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60c92-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="60c92-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60c92-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="60c92-134">INPUTS</span></span>

### <span data-ttu-id="60c92-135">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. ıpostgresqlidentity</span><span class="sxs-lookup"><span data-stu-id="60c92-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="60c92-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="60c92-136">OUTPUTS</span></span>

### <span data-ttu-id="60c92-137">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. Api20171201. ıfirewallrule</span><span class="sxs-lookup"><span data-stu-id="60c92-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="60c92-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="60c92-138">NOTES</span></span>

<span data-ttu-id="60c92-139">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="60c92-139">ALIASES</span></span>

<span data-ttu-id="60c92-140">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="60c92-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="60c92-141">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="60c92-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="60c92-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="60c92-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="60c92-143">INPUTOBJECT <IPostgreSqlIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="60c92-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="60c92-144">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="60c92-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="60c92-145">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="60c92-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="60c92-146">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="60c92-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="60c92-147">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="60c92-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="60c92-148">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="60c92-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="60c92-149">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="60c92-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="60c92-150">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="60c92-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="60c92-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="60c92-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="60c92-152">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="60c92-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="60c92-153">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="60c92-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="60c92-154">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="60c92-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="60c92-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="60c92-155">RELATED LINKS</span></span>

