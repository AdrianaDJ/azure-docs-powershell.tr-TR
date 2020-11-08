---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
ms.openlocfilehash: 71fb10b0aeed85a716a834b42b1bdae3e5f7b270
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108780"
---
# <span data-ttu-id="0d66c-101">Get-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="0d66c-101">Get-AzPostgreSqlServer</span></span>

## <span data-ttu-id="0d66c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d66c-102">SYNOPSIS</span></span>
<span data-ttu-id="0d66c-103">Sunucu hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0d66c-103">Gets information about a server.</span></span>

## <span data-ttu-id="0d66c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d66c-104">SYNTAX</span></span>

### <span data-ttu-id="0d66c-105">List1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0d66c-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0d66c-106">Al</span><span class="sxs-lookup"><span data-stu-id="0d66c-106">Get</span></span>
```
Get-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0d66c-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="0d66c-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0d66c-108">Listeniz</span><span class="sxs-lookup"><span data-stu-id="0d66c-108">List</span></span>
```
Get-AzPostgreSqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d66c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d66c-109">DESCRIPTION</span></span>
<span data-ttu-id="0d66c-110">Sunucu hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0d66c-110">Gets information about a server.</span></span>

## <span data-ttu-id="0d66c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d66c-111">EXAMPLES</span></span>

### <span data-ttu-id="0d66c-112">Örnek 1: varsayılan bağlamıyla PostgreSql sunucusunu alma</span><span class="sxs-lookup"><span data-stu-id="0d66c-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="0d66c-113">Bu cmdlet, PostgreSql sunucusunu varsayılan içerikle alır.</span><span class="sxs-lookup"><span data-stu-id="0d66c-113">This cmdlet gets PostgreSql server with default context.</span></span>

### <span data-ttu-id="0d66c-114">Örnek 2: kaynak grubuna ve sunucu adına göre PostgreSql sunucusunu alma</span><span class="sxs-lookup"><span data-stu-id="0d66c-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="0d66c-115">Bu cmdlet, PostgreSql sunucusunu kaynak grubuna ve sunucu adına göre alır.</span><span class="sxs-lookup"><span data-stu-id="0d66c-115">This cmdlet gets PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="0d66c-116">Örnek 3: belirtilen kaynak grubundaki tüm PostgreSql sunucularını listeler</span><span class="sxs-lookup"><span data-stu-id="0d66c-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="0d66c-117">Bu cmdlet, belirtilen kaynak grubundaki tüm PostgreSql sunucularını listeler.</span><span class="sxs-lookup"><span data-stu-id="0d66c-117">This cmdlet lists all the PostgreSql servers in specified resource group.</span></span>

### <span data-ttu-id="0d66c-118">Örnek 4: kimliğe göre PostgreSql sunucusunu alma</span><span class="sxs-lookup"><span data-stu-id="0d66c-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/postgresqltestserver"
PS C:\> Get-AzPostgreSqlServer -InputObject $ID

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="0d66c-119">Bu cmdlet listeleri, PostgreSql sunucusunu kimlik ile alır.</span><span class="sxs-lookup"><span data-stu-id="0d66c-119">This cmdlet lists gets PostgreSql server by identity.</span></span>

## <span data-ttu-id="0d66c-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d66c-120">PARAMETERS</span></span>

### <span data-ttu-id="0d66c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d66c-121">-DefaultProfile</span></span>
<span data-ttu-id="0d66c-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0d66c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d66c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d66c-123">-InputObject</span></span>
<span data-ttu-id="0d66c-124">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0d66c-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0d66c-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="0d66c-125">-Name</span></span>
<span data-ttu-id="0d66c-126">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="0d66c-126">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d66c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d66c-127">-ResourceGroupName</span></span>
<span data-ttu-id="0d66c-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0d66c-128">The name of the resource group.</span></span>
<span data-ttu-id="0d66c-129">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="0d66c-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0d66c-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="0d66c-130">-SubscriptionId</span></span>
<span data-ttu-id="0d66c-131">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0d66c-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d66c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d66c-132">CommonParameters</span></span>
<span data-ttu-id="0d66c-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d66c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d66c-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0d66c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d66c-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d66c-135">INPUTS</span></span>

### <span data-ttu-id="0d66c-136">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. ıpostgresqlidentity</span><span class="sxs-lookup"><span data-stu-id="0d66c-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="0d66c-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d66c-137">OUTPUTS</span></span>

### <span data-ttu-id="0d66c-138">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="0d66c-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="0d66c-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d66c-139">NOTES</span></span>

<span data-ttu-id="0d66c-140">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="0d66c-140">ALIASES</span></span>

<span data-ttu-id="0d66c-141">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="0d66c-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0d66c-142">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0d66c-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0d66c-143">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0d66c-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0d66c-144">INPUTOBJECT <IPostgreSqlIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="0d66c-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0d66c-145">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="0d66c-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0d66c-146">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="0d66c-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0d66c-147">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="0d66c-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0d66c-148">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="0d66c-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0d66c-149">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="0d66c-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0d66c-150">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0d66c-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0d66c-151">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="0d66c-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="0d66c-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="0d66c-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0d66c-153">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="0d66c-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0d66c-154">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0d66c-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0d66c-155">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="0d66c-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0d66c-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d66c-156">RELATED LINKS</span></span>

