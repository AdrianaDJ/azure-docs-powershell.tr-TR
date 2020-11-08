---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: c4eb244dd2d1a0d685bf18f39deedf9992b5597e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278399"
---
# <span data-ttu-id="36588-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="36588-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="36588-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36588-102">SYNOPSIS</span></span>
<span data-ttu-id="36588-103">Sunucunun yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="36588-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="36588-104">Update-AzMySqlServer, \ \ Loginpassword, STB vb. güncelleştirme istiyorsanız kullanın.</span><span class="sxs-lookup"><span data-stu-id="36588-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="36588-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36588-105">SYNTAX</span></span>

### <span data-ttu-id="36588-106">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="36588-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="36588-107">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="36588-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="36588-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="36588-108">DESCRIPTION</span></span>
<span data-ttu-id="36588-109">Sunucunun yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="36588-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="36588-110">Update-AzMySqlServer, \ \ Loginpassword, STB vb. güncelleştirme istiyorsanız kullanın.</span><span class="sxs-lookup"><span data-stu-id="36588-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="36588-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36588-111">EXAMPLES</span></span>

### <span data-ttu-id="36588-112">Örnek 1: MySql yapılandırmasını adıyla güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="36588-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="36588-113">Bu cmdlet, MySql yapılandırmasını adıyla günceller.</span><span class="sxs-lookup"><span data-stu-id="36588-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="36588-114">Örnek 2: MySql yapılandırmasını kimlik ile güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="36588-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="36588-115">Bu cmdlet 'ler, kimliğe göre MySql yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="36588-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="36588-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36588-116">PARAMETERS</span></span>

### <span data-ttu-id="36588-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="36588-117">-AsJob</span></span>
<span data-ttu-id="36588-118">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="36588-118">Run the command as a job</span></span>

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

### <span data-ttu-id="36588-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36588-119">-DefaultProfile</span></span>
<span data-ttu-id="36588-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="36588-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36588-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36588-121">-InputObject</span></span>
<span data-ttu-id="36588-122">Kimlik parametresi.</span><span class="sxs-lookup"><span data-stu-id="36588-122">Identity Parameter.</span></span>
<span data-ttu-id="36588-123">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="36588-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36588-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="36588-124">-Name</span></span>
<span data-ttu-id="36588-125">Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="36588-125">The name of the server configuration.</span></span>

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

### <span data-ttu-id="36588-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="36588-126">-NoWait</span></span>
<span data-ttu-id="36588-127">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="36588-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="36588-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36588-128">-ResourceGroupName</span></span>
<span data-ttu-id="36588-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="36588-129">The name of the resource group.</span></span>
<span data-ttu-id="36588-130">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="36588-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="36588-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="36588-131">-ServerName</span></span>
<span data-ttu-id="36588-132">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="36588-132">The name of the server.</span></span>

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

### <span data-ttu-id="36588-133">-Kaynak</span><span class="sxs-lookup"><span data-stu-id="36588-133">-Source</span></span>
<span data-ttu-id="36588-134">Yapılandırmanın kaynağı.</span><span class="sxs-lookup"><span data-stu-id="36588-134">Source of the configuration.</span></span>

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

### <span data-ttu-id="36588-135">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="36588-135">-SubscriptionId</span></span>
<span data-ttu-id="36588-136">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="36588-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="36588-137">-Değer</span><span class="sxs-lookup"><span data-stu-id="36588-137">-Value</span></span>
<span data-ttu-id="36588-138">Yapılandırmanın değeri.</span><span class="sxs-lookup"><span data-stu-id="36588-138">Value of the configuration.</span></span>

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

### <span data-ttu-id="36588-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="36588-139">-Confirm</span></span>
<span data-ttu-id="36588-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="36588-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36588-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36588-141">-WhatIf</span></span>
<span data-ttu-id="36588-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="36588-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36588-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="36588-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36588-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36588-144">CommonParameters</span></span>
<span data-ttu-id="36588-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36588-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36588-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="36588-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36588-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36588-147">INPUTS</span></span>

### <span data-ttu-id="36588-148">Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Sanysqlidentity</span><span class="sxs-lookup"><span data-stu-id="36588-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="36588-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36588-149">OUTPUTS</span></span>

### <span data-ttu-id="36588-150">Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Api20171201. Iconation</span><span class="sxs-lookup"><span data-stu-id="36588-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="36588-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36588-151">NOTES</span></span>

<span data-ttu-id="36588-152">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="36588-152">ALIASES</span></span>

<span data-ttu-id="36588-153">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="36588-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="36588-154">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="36588-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="36588-155">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="36588-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="36588-156">INPUTOBJECT <IMySqlIdentity> : IDENTITY parametresi.</span><span class="sxs-lookup"><span data-stu-id="36588-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="36588-157">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="36588-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="36588-158">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="36588-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="36588-159">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="36588-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="36588-160">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="36588-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="36588-161">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="36588-161">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="36588-162">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="36588-162">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="36588-163">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="36588-163">The name is case insensitive.</span></span>
  - <span data-ttu-id="36588-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="36588-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="36588-165">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="36588-165">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="36588-166">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="36588-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="36588-167">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="36588-167">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="36588-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36588-168">RELATED LINKS</span></span>

