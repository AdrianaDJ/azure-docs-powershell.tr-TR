---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
ms.openlocfilehash: b92390969c4650d60d5c4a6954520fbbf3f26c71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274413"
---
# <span data-ttu-id="4a4f9-101">Get-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a4f9-101">Get-AzMySqlConfiguration</span></span>

## <span data-ttu-id="4a4f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a4f9-102">SYNOPSIS</span></span>
<span data-ttu-id="4a4f9-103">Sunucu yapılandırması hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="4a4f9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a4f9-104">SYNTAX</span></span>

### <span data-ttu-id="4a4f9-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4a4f9-105">List (Default)</span></span>
```
Get-AzMySqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4a4f9-106">Al</span><span class="sxs-lookup"><span data-stu-id="4a4f9-106">Get</span></span>
```
Get-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4a4f9-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="4a4f9-107">GetViaIdentity</span></span>
```
Get-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4a4f9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a4f9-108">DESCRIPTION</span></span>
<span data-ttu-id="4a4f9-109">Sunucu yapılandırması hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="4a4f9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a4f9-110">EXAMPLES</span></span>

### <span data-ttu-id="4a4f9-111">Örnek 1: belirtilen MySql sunucusundaki tüm yapılandırmaları listeler</span><span class="sxs-lookup"><span data-stu-id="4a4f9-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name                                     Type
----                                     ----
audit_log_enabled                        Microsoft.DBforMySQL/servers/configurations
audit_log_events                         Microsoft.DBforMySQL/servers/configurations
audit_log_exclude_users                  Microsoft.DBforMySQL/servers/configurations
audit_log_include_users                  Microsoft.DBforMySQL/servers/configurations
...
transaction_prealloc_size                Microsoft.DBforMySQL/servers/configurations
tx_isolation                             Microsoft.DBforMySQL/servers/configurations
updatable_views_with_limit               Microsoft.DBforMySQL/servers/configurations
wait_timeout                             Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="4a4f9-112">Bu cmdlet belirtilen MySql sunucusundaki tüm yapılandırmaları listeler.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="4a4f9-113">Örnek 2: belirtilen MySql yapılandırmasını ada göre alma</span><span class="sxs-lookup"><span data-stu-id="4a4f9-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -Name time_zone -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name      Type
----      ----
time_zone Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="4a4f9-114">Bu cmdlet belirtilen MySql yapılandırmasını ada göre alır.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-114">This cmdlet gets specified MySql configuration by name.</span></span>

## <span data-ttu-id="4a4f9-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a4f9-115">PARAMETERS</span></span>

### <span data-ttu-id="4a4f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a4f9-116">-DefaultProfile</span></span>
<span data-ttu-id="4a4f9-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a4f9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a4f9-118">-InputObject</span></span>
<span data-ttu-id="4a4f9-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4a4f9-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="4a4f9-120">-Name</span></span>
<span data-ttu-id="4a4f9-121">Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-121">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a4f9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a4f9-122">-ResourceGroupName</span></span>
<span data-ttu-id="4a4f9-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-123">The name of the resource group.</span></span>
<span data-ttu-id="4a4f9-124">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4a4f9-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4a4f9-125">-ServerName</span></span>
<span data-ttu-id="4a4f9-126">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-126">The name of the server.</span></span>

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

### <span data-ttu-id="4a4f9-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="4a4f9-127">-SubscriptionId</span></span>
<span data-ttu-id="4a4f9-128">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4a4f9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a4f9-129">CommonParameters</span></span>
<span data-ttu-id="4a4f9-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a4f9-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a4f9-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a4f9-132">INPUTS</span></span>

### <span data-ttu-id="4a4f9-133">Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Sanysqlidentity</span><span class="sxs-lookup"><span data-stu-id="4a4f9-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="4a4f9-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a4f9-134">OUTPUTS</span></span>

### <span data-ttu-id="4a4f9-135">Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Api20171201. Iconation</span><span class="sxs-lookup"><span data-stu-id="4a4f9-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="4a4f9-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a4f9-136">NOTES</span></span>

<span data-ttu-id="4a4f9-137">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="4a4f9-137">ALIASES</span></span>

<span data-ttu-id="4a4f9-138">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="4a4f9-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4a4f9-139">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4a4f9-140">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4a4f9-141">INPUTOBJECT <IMySqlIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="4a4f9-141">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4a4f9-142">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4a4f9-143">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4a4f9-144">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4a4f9-145">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="4a4f9-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4a4f9-146">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4a4f9-147">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4a4f9-148">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="4a4f9-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4a4f9-150">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4a4f9-151">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4a4f9-152">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4a4f9-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a4f9-153">RELATED LINKS</span></span>

