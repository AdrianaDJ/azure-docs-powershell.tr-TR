---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 7ae1159c3cd5f5feea3d836a421dd9fe08c78da8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267287"
---
# <span data-ttu-id="c8d8b-101">Get-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c8d8b-101">Get-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="c8d8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d8b-103">Sanal ağ kuralı alır.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="c8d8b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c8d8b-104">SYNTAX</span></span>

### <span data-ttu-id="c8d8b-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c8d8b-105">List (Default)</span></span>
```
Get-AzMariaDbVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="c8d8b-106">Al</span><span class="sxs-lookup"><span data-stu-id="c8d8b-106">Get</span></span>
```
Get-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="c8d8b-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="c8d8b-107">GetViaIdentity</span></span>
```
Get-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="c8d8b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8d8b-108">DESCRIPTION</span></span>
<span data-ttu-id="c8d8b-109">Sanal ağ kuralı alır.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="c8d8b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c8d8b-110">EXAMPLES</span></span>

### <span data-ttu-id="c8d8b-111">Örnek 1: bir Mari</span><span class="sxs-lookup"><span data-stu-id="c8d8b-111">Example 1: List all virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
vnetrule-Adsefc Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="c8d8b-112">Bu komut, bir MariaDB 'ın altındaki tüm sanal ağ kuralını listeler.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-112">This command lists all virtual network rule under a MariaDB.</span></span>

### <span data-ttu-id="c8d8b-113">Örnek 2: bir Marialtında sanal ağ kuralı alın</span><span class="sxs-lookup"><span data-stu-id="c8d8b-113">Example 2: Get virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn -Name vnetrule-QdMJpU

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="c8d8b-114">Bu komut, bir MariaDB altında sanal ağ kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-114">This command gets virtual network rule under a MariaDB.</span></span>

## <span data-ttu-id="c8d8b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c8d8b-115">PARAMETERS</span></span>

### <span data-ttu-id="c8d8b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8d8b-116">-DefaultProfile</span></span>
<span data-ttu-id="c8d8b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8d8b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8d8b-118">-InputObject</span></span>
<span data-ttu-id="c8d8b-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c8d8b-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="c8d8b-120">-Name</span></span>
<span data-ttu-id="c8d8b-121">Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-121">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="c8d8b-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c8d8b-122">-PassThru</span></span>
<span data-ttu-id="c8d8b-123">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="c8d8b-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c8d8b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8d8b-124">-ResourceGroupName</span></span>
<span data-ttu-id="c8d8b-125">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c8d8b-126">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c8d8b-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c8d8b-127">-ServerName</span></span>
<span data-ttu-id="c8d8b-128">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-128">The name of the server.</span></span>

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

### <span data-ttu-id="c8d8b-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c8d8b-129">-SubscriptionId</span></span>
<span data-ttu-id="c8d8b-130">Bir Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-130">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="c8d8b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d8b-131">CommonParameters</span></span>
<span data-ttu-id="c8d8b-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d8b-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d8b-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c8d8b-134">INPUTS</span></span>

### <span data-ttu-id="c8d8b-135">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Sanarladbıdentity</span><span class="sxs-lookup"><span data-stu-id="c8d8b-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="c8d8b-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c8d8b-136">OUTPUTS</span></span>

### <span data-ttu-id="c8d8b-137">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Api20180601Preview. ıvirtualnetworkrule</span><span class="sxs-lookup"><span data-stu-id="c8d8b-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="c8d8b-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c8d8b-138">NOTES</span></span>

<span data-ttu-id="c8d8b-139">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="c8d8b-139">ALIASES</span></span>

<span data-ttu-id="c8d8b-140">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="c8d8b-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c8d8b-141">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c8d8b-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c8d8b-143">INPUTOBJECT <IMariaDbIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="c8d8b-143">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c8d8b-144">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="c8d8b-145">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c8d8b-146">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="c8d8b-147">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="c8d8b-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c8d8b-148">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="c8d8b-149">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="c8d8b-150">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="c8d8b-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="c8d8b-152">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="c8d8b-153">`[SubscriptionId <String>]`: Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-153">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="c8d8b-154">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="c8d8b-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c8d8b-155">RELATED LINKS</span></span>

