---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
ms.openlocfilehash: 4ee32822f6fb4872a9fa01d020ed0f0bf92b0456
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273526"
---
# <span data-ttu-id="ca1fe-101">Update-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca1fe-101">Update-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="ca1fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca1fe-102">SYNOPSIS</span></span>
<span data-ttu-id="ca1fe-103">Sunucunun yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="ca1fe-104">Update-AzMariaDbServer, \ \ Loginpassword, STB vb. güncelleştirme istiyorsanız kullanın.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-104">Use Update-AzMariaDbServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="ca1fe-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca1fe-105">SYNTAX</span></span>

### <span data-ttu-id="ca1fe-106">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ca1fe-106">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ca1fe-107">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="ca1fe-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ca1fe-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca1fe-108">DESCRIPTION</span></span>
<span data-ttu-id="ca1fe-109">Sunucunun yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="ca1fe-110">Update-AzMariaDberver, \ \ Loginpassword, STB vb. güncelleştirme istiyorsanız kullanın.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-110">Use Update-AzMariaDberver instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="ca1fe-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca1fe-111">EXAMPLES</span></span>

### <span data-ttu-id="ca1fe-112">Örnek 1: MariaDB yapılandırmasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ca1fe-112">Example 1: Update MariaDB configuration</span></span>
```powershell
PS C:\> Update-AzMariaDbConfiguration -Name delayed_insert_timeout -Value 200 -ServerName mariadb-test-h3pame -ResourceGroupName mariadb-test-qu5ov0 

Name                   Type
----                   ----
delayed_insert_timeout Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="ca1fe-113">Bu komut bir MariaDB yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-113">This command updates a MariaDB configuration.</span></span>

## <span data-ttu-id="ca1fe-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca1fe-114">PARAMETERS</span></span>

### <span data-ttu-id="ca1fe-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="ca1fe-115">-AsJob</span></span>
<span data-ttu-id="ca1fe-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="ca1fe-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ca1fe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca1fe-117">-DefaultProfile</span></span>
<span data-ttu-id="ca1fe-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca1fe-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca1fe-119">-InputObject</span></span>
<span data-ttu-id="ca1fe-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca1fe-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="ca1fe-121">-Name</span></span>
<span data-ttu-id="ca1fe-122">Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="ca1fe-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ca1fe-123">-NoWait</span></span>
<span data-ttu-id="ca1fe-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="ca1fe-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ca1fe-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca1fe-125">-ResourceGroupName</span></span>
<span data-ttu-id="ca1fe-126">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ca1fe-127">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ca1fe-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ca1fe-128">-ServerName</span></span>
<span data-ttu-id="ca1fe-129">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-129">The name of the server.</span></span>

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

### <span data-ttu-id="ca1fe-130">-Kaynak</span><span class="sxs-lookup"><span data-stu-id="ca1fe-130">-Source</span></span>
<span data-ttu-id="ca1fe-131">Yapılandırmanın kaynağı.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-131">Source of the configuration.</span></span>

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

### <span data-ttu-id="ca1fe-132">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ca1fe-132">-SubscriptionId</span></span>
<span data-ttu-id="ca1fe-133">Bir Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-133">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="ca1fe-134">-Değer</span><span class="sxs-lookup"><span data-stu-id="ca1fe-134">-Value</span></span>
<span data-ttu-id="ca1fe-135">Yapılandırmanın değeri.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-135">Value of the configuration.</span></span>

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

### <span data-ttu-id="ca1fe-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="ca1fe-136">-Confirm</span></span>
<span data-ttu-id="ca1fe-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca1fe-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca1fe-138">-WhatIf</span></span>
<span data-ttu-id="ca1fe-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca1fe-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca1fe-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca1fe-141">CommonParameters</span></span>
<span data-ttu-id="ca1fe-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca1fe-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca1fe-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca1fe-144">INPUTS</span></span>

### <span data-ttu-id="ca1fe-145">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Sanarladbıdentity</span><span class="sxs-lookup"><span data-stu-id="ca1fe-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="ca1fe-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca1fe-146">OUTPUTS</span></span>

### <span data-ttu-id="ca1fe-147">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Api20180601Preview. Iconation</span><span class="sxs-lookup"><span data-stu-id="ca1fe-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="ca1fe-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca1fe-148">NOTES</span></span>

<span data-ttu-id="ca1fe-149">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="ca1fe-149">ALIASES</span></span>

<span data-ttu-id="ca1fe-150">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="ca1fe-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ca1fe-151">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ca1fe-152">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ca1fe-153">INPUTOBJECT <IMariaDbIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="ca1fe-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ca1fe-154">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ca1fe-155">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ca1fe-156">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ca1fe-157">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="ca1fe-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ca1fe-158">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ca1fe-159">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ca1fe-160">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ca1fe-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ca1fe-162">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ca1fe-163">`[SubscriptionId <String>]`: Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="ca1fe-164">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="ca1fe-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ca1fe-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca1fe-165">RELATED LINKS</span></span>

