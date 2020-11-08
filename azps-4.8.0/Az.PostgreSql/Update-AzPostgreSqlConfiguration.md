---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
ms.openlocfilehash: e1b0ea3d07a7504e75f8bd6143820c52e73d9cf9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265819"
---
# <span data-ttu-id="d27e2-101">Update-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d27e2-101">Update-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="d27e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d27e2-102">SYNOPSIS</span></span>
<span data-ttu-id="d27e2-103">Sunucunun yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d27e2-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="d27e2-104">Update-AzPostgreSqlServer, \ \ Loginpassword, STB vb. güncelleştirme istiyorsanız kullanın.</span><span class="sxs-lookup"><span data-stu-id="d27e2-104">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="d27e2-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d27e2-105">SYNTAX</span></span>

### <span data-ttu-id="d27e2-106">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d27e2-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d27e2-107">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="d27e2-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d27e2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d27e2-108">DESCRIPTION</span></span>
<span data-ttu-id="d27e2-109">Sunucunun yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d27e2-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="d27e2-110">Update-AzPostgreSqlServer, \ \ Loginpassword, STB vb. güncelleştirme istiyorsanız kullanın.</span><span class="sxs-lookup"><span data-stu-id="d27e2-110">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="d27e2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d27e2-111">EXAMPLES</span></span>

### <span data-ttu-id="d27e2-112">Örnek 1: PostgreSql yapılandırmasını adıyla güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d27e2-112">Example 1: Update PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlConfiguration -Name intervalstyle -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -Value SQL_STANDARD

Name          Value
----          -----
intervalstyle SQL_STANDARD
```

<span data-ttu-id="d27e2-113">Bu cmdlet, PostgreSql yapılandırmasını adıyla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d27e2-113">This cmdlet updates PostgreSql configuration by name.</span></span>

### <span data-ttu-id="d27e2-114">Örnek 2: kimliği kullanarak PostgreSql yapılandırmasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="d27e2-114">Example 2: Update PostgreSql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/configurations/deadlock_timeout"
PS C:\> Update-AzPostgreSqlConfiguration -InputObject $ID -Value 2000

Name             Value
----             -----
deadlock_timeout 2000
```

<span data-ttu-id="d27e2-115">Bu cmdlet 'ler kimliği kullanarak PostgreSql yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d27e2-115">These cmdlets update PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="d27e2-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d27e2-116">PARAMETERS</span></span>

### <span data-ttu-id="d27e2-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="d27e2-117">-AsJob</span></span>
<span data-ttu-id="d27e2-118">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="d27e2-118">Run the command as a job</span></span>

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

### <span data-ttu-id="d27e2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d27e2-119">-DefaultProfile</span></span>
<span data-ttu-id="d27e2-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d27e2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d27e2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d27e2-121">-InputObject</span></span>
<span data-ttu-id="d27e2-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d27e2-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d27e2-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="d27e2-123">-Name</span></span>
<span data-ttu-id="d27e2-124">Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="d27e2-124">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d27e2-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d27e2-125">-NoWait</span></span>
<span data-ttu-id="d27e2-126">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="d27e2-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d27e2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d27e2-127">-ResourceGroupName</span></span>
<span data-ttu-id="d27e2-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d27e2-128">The name of the resource group.</span></span>
<span data-ttu-id="d27e2-129">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="d27e2-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d27e2-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d27e2-130">-ServerName</span></span>
<span data-ttu-id="d27e2-131">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="d27e2-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d27e2-132">-Kaynak</span><span class="sxs-lookup"><span data-stu-id="d27e2-132">-Source</span></span>
<span data-ttu-id="d27e2-133">Yapılandırmanın kaynağı.</span><span class="sxs-lookup"><span data-stu-id="d27e2-133">Source of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d27e2-134">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d27e2-134">-SubscriptionId</span></span>
<span data-ttu-id="d27e2-135">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d27e2-135">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d27e2-136">-Değer</span><span class="sxs-lookup"><span data-stu-id="d27e2-136">-Value</span></span>
<span data-ttu-id="d27e2-137">Yapılandırmanın değeri.</span><span class="sxs-lookup"><span data-stu-id="d27e2-137">Value of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d27e2-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="d27e2-138">-Confirm</span></span>
<span data-ttu-id="d27e2-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d27e2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d27e2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d27e2-140">-WhatIf</span></span>
<span data-ttu-id="d27e2-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d27e2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d27e2-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d27e2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d27e2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d27e2-143">CommonParameters</span></span>
<span data-ttu-id="d27e2-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d27e2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d27e2-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d27e2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d27e2-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d27e2-146">INPUTS</span></span>

### <span data-ttu-id="d27e2-147">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. ıpostgresqlidentity</span><span class="sxs-lookup"><span data-stu-id="d27e2-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="d27e2-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d27e2-148">OUTPUTS</span></span>

### <span data-ttu-id="d27e2-149">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. Api20171201. Iconation</span><span class="sxs-lookup"><span data-stu-id="d27e2-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="d27e2-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d27e2-150">NOTES</span></span>

<span data-ttu-id="d27e2-151">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="d27e2-151">ALIASES</span></span>

<span data-ttu-id="d27e2-152">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="d27e2-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d27e2-153">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d27e2-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d27e2-154">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d27e2-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d27e2-155">INPUTOBJECT <IPostgreSqlIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="d27e2-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d27e2-156">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="d27e2-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d27e2-157">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="d27e2-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d27e2-158">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="d27e2-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d27e2-159">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="d27e2-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d27e2-160">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="d27e2-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d27e2-161">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d27e2-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d27e2-162">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="d27e2-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="d27e2-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="d27e2-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d27e2-164">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="d27e2-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d27e2-165">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d27e2-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d27e2-166">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="d27e2-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d27e2-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d27e2-167">RELATED LINKS</span></span>

