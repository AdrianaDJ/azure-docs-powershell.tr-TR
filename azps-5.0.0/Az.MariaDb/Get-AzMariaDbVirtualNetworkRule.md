---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 7ae1159c3cd5f5feea3d836a421dd9fe08c78da8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278902"
---
# <span data-ttu-id="ec0ab-101">Get-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ec0ab-101">Get-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="ec0ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec0ab-102">SYNOPSIS</span></span>
<span data-ttu-id="ec0ab-103">Sanal ağ kuralı alır.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="ec0ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec0ab-104">SYNTAX</span></span>

### <span data-ttu-id="ec0ab-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ec0ab-105">List (Default)</span></span>
```
Get-AzMariaDbVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="ec0ab-106">Al</span><span class="sxs-lookup"><span data-stu-id="ec0ab-106">Get</span></span>
```
Get-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="ec0ab-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="ec0ab-107">GetViaIdentity</span></span>
```
Get-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="ec0ab-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec0ab-108">DESCRIPTION</span></span>
<span data-ttu-id="ec0ab-109">Sanal ağ kuralı alır.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="ec0ab-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec0ab-110">EXAMPLES</span></span>

### <span data-ttu-id="ec0ab-111">Örnek 1: bir Mari</span><span class="sxs-lookup"><span data-stu-id="ec0ab-111">Example 1: List all virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
vnetrule-Adsefc Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="ec0ab-112">Bu komut, bir MariaDB 'ın altındaki tüm sanal ağ kuralını listeler.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-112">This command lists all virtual network rule under a MariaDB.</span></span>

### <span data-ttu-id="ec0ab-113">Örnek 2: bir Marialtında sanal ağ kuralı alın</span><span class="sxs-lookup"><span data-stu-id="ec0ab-113">Example 2: Get virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn -Name vnetrule-QdMJpU

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="ec0ab-114">Bu komut, bir MariaDB altında sanal ağ kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-114">This command gets virtual network rule under a MariaDB.</span></span>

## <span data-ttu-id="ec0ab-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec0ab-115">PARAMETERS</span></span>

### <span data-ttu-id="ec0ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec0ab-116">-DefaultProfile</span></span>
<span data-ttu-id="ec0ab-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec0ab-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec0ab-118">-InputObject</span></span>
<span data-ttu-id="ec0ab-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ec0ab-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="ec0ab-120">-Name</span></span>
<span data-ttu-id="ec0ab-121">Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-121">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="ec0ab-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ec0ab-122">-PassThru</span></span>
<span data-ttu-id="ec0ab-123">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="ec0ab-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ec0ab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec0ab-124">-ResourceGroupName</span></span>
<span data-ttu-id="ec0ab-125">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ec0ab-126">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ec0ab-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ec0ab-127">-ServerName</span></span>
<span data-ttu-id="ec0ab-128">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-128">The name of the server.</span></span>

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

### <span data-ttu-id="ec0ab-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ec0ab-129">-SubscriptionId</span></span>
<span data-ttu-id="ec0ab-130">Bir Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-130">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="ec0ab-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec0ab-131">CommonParameters</span></span>
<span data-ttu-id="ec0ab-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec0ab-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec0ab-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec0ab-134">INPUTS</span></span>

### <span data-ttu-id="ec0ab-135">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Sanarladbıdentity</span><span class="sxs-lookup"><span data-stu-id="ec0ab-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="ec0ab-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec0ab-136">OUTPUTS</span></span>

### <span data-ttu-id="ec0ab-137">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Api20180601Preview. ıvirtualnetworkrule</span><span class="sxs-lookup"><span data-stu-id="ec0ab-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="ec0ab-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec0ab-138">NOTES</span></span>

<span data-ttu-id="ec0ab-139">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="ec0ab-139">ALIASES</span></span>

<span data-ttu-id="ec0ab-140">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="ec0ab-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ec0ab-141">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ec0ab-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ec0ab-143">INPUTOBJECT <IMariaDbIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="ec0ab-143">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ec0ab-144">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ec0ab-145">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ec0ab-146">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ec0ab-147">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="ec0ab-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ec0ab-148">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ec0ab-149">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ec0ab-150">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ec0ab-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ec0ab-152">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ec0ab-153">`[SubscriptionId <String>]`: Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-153">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="ec0ab-154">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="ec0ab-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ec0ab-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec0ab-155">RELATED LINKS</span></span>

