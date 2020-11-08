---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: eb8fc13bd2c1ef4e829cf5d4626453909b6ff773
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279182"
---
# <span data-ttu-id="136e8-101">Get-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="136e8-101">Get-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="136e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="136e8-102">SYNOPSIS</span></span>
<span data-ttu-id="136e8-103">Sanal ağ kuralı alır.</span><span class="sxs-lookup"><span data-stu-id="136e8-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="136e8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="136e8-104">SYNTAX</span></span>

### <span data-ttu-id="136e8-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="136e8-105">List (Default)</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="136e8-106">Al</span><span class="sxs-lookup"><span data-stu-id="136e8-106">Get</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="136e8-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="136e8-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="136e8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="136e8-108">DESCRIPTION</span></span>
<span data-ttu-id="136e8-109">Sanal ağ kuralı alır.</span><span class="sxs-lookup"><span data-stu-id="136e8-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="136e8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="136e8-110">EXAMPLES</span></span>

### <span data-ttu-id="136e8-111">Örnek 1: belirtilen PostgreSql sunucusundaki tüm sanal ağ kurallarını listeler</span><span class="sxs-lookup"><span data-stu-id="136e8-111">Example 1: Lists all the Virtual Network Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="136e8-112">Bu cmdlet, belirtilen PostgreSql sunucusundaki tüm sanal ağ kurallarını listeler.</span><span class="sxs-lookup"><span data-stu-id="136e8-112">This cmdlet lists all the Virtual Network Rules in specified PostgreSql server.</span></span>

### <span data-ttu-id="136e8-113">Örnek 2: ada göre sanal ağ kuralı alın</span><span class="sxs-lookup"><span data-stu-id="136e8-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="136e8-114">Bu cmdlet sanal ağ kuralını adıyla alır.</span><span class="sxs-lookup"><span data-stu-id="136e8-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="136e8-115">Örnek 3: kimliğe göre sanal ağ kuralı alın</span><span class="sxs-lookup"><span data-stu-id="136e8-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="136e8-116">Bu cmdlet sanal ağ kuralını kimliğe göre alır.</span><span class="sxs-lookup"><span data-stu-id="136e8-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="136e8-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="136e8-117">PARAMETERS</span></span>

### <span data-ttu-id="136e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="136e8-118">-DefaultProfile</span></span>
<span data-ttu-id="136e8-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="136e8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="136e8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="136e8-120">-InputObject</span></span>
<span data-ttu-id="136e8-121">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="136e8-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="136e8-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="136e8-122">-Name</span></span>
<span data-ttu-id="136e8-123">Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="136e8-123">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="136e8-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="136e8-124">-PassThru</span></span>
<span data-ttu-id="136e8-125">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="136e8-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="136e8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="136e8-126">-ResourceGroupName</span></span>
<span data-ttu-id="136e8-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="136e8-127">The name of the resource group.</span></span>
<span data-ttu-id="136e8-128">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="136e8-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="136e8-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="136e8-129">-ServerName</span></span>
<span data-ttu-id="136e8-130">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="136e8-130">The name of the server.</span></span>

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

### <span data-ttu-id="136e8-131">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="136e8-131">-SubscriptionId</span></span>
<span data-ttu-id="136e8-132">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="136e8-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="136e8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="136e8-133">CommonParameters</span></span>
<span data-ttu-id="136e8-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="136e8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="136e8-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="136e8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="136e8-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="136e8-136">INPUTS</span></span>

### <span data-ttu-id="136e8-137">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. ıpostgresqlidentity</span><span class="sxs-lookup"><span data-stu-id="136e8-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="136e8-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="136e8-138">OUTPUTS</span></span>

### <span data-ttu-id="136e8-139">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. Api20171201. ıvirtualnetworkrule</span><span class="sxs-lookup"><span data-stu-id="136e8-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="136e8-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="136e8-140">NOTES</span></span>

<span data-ttu-id="136e8-141">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="136e8-141">ALIASES</span></span>

<span data-ttu-id="136e8-142">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="136e8-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="136e8-143">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="136e8-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="136e8-144">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="136e8-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="136e8-145">INPUTOBJECT <IPostgreSqlIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="136e8-145">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="136e8-146">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="136e8-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="136e8-147">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="136e8-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="136e8-148">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="136e8-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="136e8-149">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="136e8-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="136e8-150">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="136e8-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="136e8-151">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="136e8-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="136e8-152">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="136e8-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="136e8-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="136e8-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="136e8-154">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="136e8-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="136e8-155">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="136e8-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="136e8-156">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="136e8-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="136e8-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="136e8-157">RELATED LINKS</span></span>

