---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
ms.openlocfilehash: 7fdc31b4a64733ce686b38ccfb176f754f3f84ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277929"
---
# <span data-ttu-id="6479e-101">Get-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="6479e-101">Get-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="6479e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6479e-102">SYNOPSIS</span></span>
<span data-ttu-id="6479e-103">Sunucu yapılandırması hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="6479e-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="6479e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6479e-104">SYNTAX</span></span>

### <span data-ttu-id="6479e-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6479e-105">List (Default)</span></span>
```
Get-AzPostgreSqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6479e-106">Al</span><span class="sxs-lookup"><span data-stu-id="6479e-106">Get</span></span>
```
Get-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6479e-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="6479e-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6479e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6479e-108">DESCRIPTION</span></span>
<span data-ttu-id="6479e-109">Sunucu yapılandırması hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="6479e-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="6479e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6479e-110">EXAMPLES</span></span>

### <span data-ttu-id="6479e-111">Örnek 1: PostgreSql sunucusundaki tüm yapılandırmaları listeler</span><span class="sxs-lookup"><span data-stu-id="6479e-111">Example 1: List all configurations in PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                                  Value
----                                  -----
array_nulls                           on
backslash_quote                       safe_encoding
bytea_output                          hex
check_function_bodies                 on
client_encoding                       sql_ascii
...
azure.replication_support             REPLICA
max_wal_senders                       10
max_replication_slots                 10
hot_standby_feedback                  off
logging_collector                     on
```

<span data-ttu-id="6479e-112">Bu cmdlet, belirtilen PostgreSql Server 'daki tüm konfigürasyonları listeler.</span><span class="sxs-lookup"><span data-stu-id="6479e-112">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

### <span data-ttu-id="6479e-113">Örnek 2: belirtilen PostgreSql yapılandırmasını adıyla alma</span><span class="sxs-lookup"><span data-stu-id="6479e-113">Example 2: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -Name timezone -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name     Value
----     -----
timezone UTC
```

<span data-ttu-id="6479e-114">Bu cmdlet, belirtilen PostgreSql yapılandırmasını adıyla alır.</span><span class="sxs-lookup"><span data-stu-id="6479e-114">This cmdlet gets specified PostgreSql configuration by name.</span></span>

## <span data-ttu-id="6479e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6479e-115">PARAMETERS</span></span>

### <span data-ttu-id="6479e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6479e-116">-DefaultProfile</span></span>
<span data-ttu-id="6479e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6479e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6479e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6479e-118">-InputObject</span></span>
<span data-ttu-id="6479e-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6479e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6479e-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="6479e-120">-Name</span></span>
<span data-ttu-id="6479e-121">Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="6479e-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="6479e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6479e-122">-ResourceGroupName</span></span>
<span data-ttu-id="6479e-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6479e-123">The name of the resource group.</span></span>
<span data-ttu-id="6479e-124">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="6479e-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6479e-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6479e-125">-ServerName</span></span>
<span data-ttu-id="6479e-126">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="6479e-126">The name of the server.</span></span>

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

### <span data-ttu-id="6479e-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="6479e-127">-SubscriptionId</span></span>
<span data-ttu-id="6479e-128">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6479e-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6479e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6479e-129">CommonParameters</span></span>
<span data-ttu-id="6479e-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6479e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6479e-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6479e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6479e-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6479e-132">INPUTS</span></span>

### <span data-ttu-id="6479e-133">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. ıpostgresqlidentity</span><span class="sxs-lookup"><span data-stu-id="6479e-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="6479e-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6479e-134">OUTPUTS</span></span>

### <span data-ttu-id="6479e-135">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. Api20171201. Iconation</span><span class="sxs-lookup"><span data-stu-id="6479e-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="6479e-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6479e-136">NOTES</span></span>

<span data-ttu-id="6479e-137">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="6479e-137">ALIASES</span></span>

<span data-ttu-id="6479e-138">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="6479e-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6479e-139">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6479e-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6479e-140">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6479e-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6479e-141">INPUTOBJECT <IPostgreSqlIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="6479e-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6479e-142">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="6479e-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6479e-143">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="6479e-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6479e-144">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="6479e-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6479e-145">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="6479e-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6479e-146">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="6479e-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6479e-147">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6479e-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6479e-148">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="6479e-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="6479e-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="6479e-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6479e-150">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="6479e-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6479e-151">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6479e-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6479e-152">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="6479e-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6479e-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6479e-153">RELATED LINKS</span></span>

