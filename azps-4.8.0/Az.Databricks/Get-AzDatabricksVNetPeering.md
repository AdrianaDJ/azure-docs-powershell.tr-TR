---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: d5078ac91627cdf9f7b57801e3b7a958b9bd776e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273633"
---
# <span data-ttu-id="7405f-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="7405f-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="7405f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7405f-102">SYNOPSIS</span></span>
<span data-ttu-id="7405f-103">Çalışma alanı vNet eşliğini alır.</span><span class="sxs-lookup"><span data-stu-id="7405f-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="7405f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7405f-104">SYNTAX</span></span>

### <span data-ttu-id="7405f-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7405f-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7405f-106">Al</span><span class="sxs-lookup"><span data-stu-id="7405f-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="7405f-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="7405f-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="7405f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7405f-108">DESCRIPTION</span></span>
<span data-ttu-id="7405f-109">Çalışma alanı vNet eşliğini alır.</span><span class="sxs-lookup"><span data-stu-id="7405f-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="7405f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7405f-110">EXAMPLES</span></span>

### <span data-ttu-id="7405f-111">Örnek 1: bir verieşleri altındaki tüm VNET eşliğini listeler</span><span class="sxs-lookup"><span data-stu-id="7405f-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="7405f-112">Bu komut, bir verieşleri altındaki tüm VNET eşliğini listeler.</span><span class="sxs-lookup"><span data-stu-id="7405f-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="7405f-113">Örnek 2: VNET eşlemesi alma</span><span class="sxs-lookup"><span data-stu-id="7405f-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="7405f-114">Bu komut VNET eşlemesi alır.</span><span class="sxs-lookup"><span data-stu-id="7405f-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="7405f-115">Örnek 3: nesneye göre VNET eşlemesi alma</span><span class="sxs-lookup"><span data-stu-id="7405f-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="7405f-116">Bu komut, nesneden bir VNET eşlemesi alır.</span><span class="sxs-lookup"><span data-stu-id="7405f-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="7405f-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7405f-117">PARAMETERS</span></span>

### <span data-ttu-id="7405f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7405f-118">-DefaultProfile</span></span>
<span data-ttu-id="7405f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7405f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7405f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7405f-120">-InputObject</span></span>
<span data-ttu-id="7405f-121">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7405f-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7405f-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="7405f-122">-Name</span></span>
<span data-ttu-id="7405f-123">Çalışma alanı vNet eşlemesi adı.</span><span class="sxs-lookup"><span data-stu-id="7405f-123">The name of the workspace vNet peering.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7405f-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7405f-124">-PassThru</span></span>
<span data-ttu-id="7405f-125">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="7405f-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7405f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7405f-126">-ResourceGroupName</span></span>
<span data-ttu-id="7405f-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7405f-127">The name of the resource group.</span></span>
<span data-ttu-id="7405f-128">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="7405f-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7405f-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="7405f-129">-SubscriptionId</span></span>
<span data-ttu-id="7405f-130">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7405f-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7405f-131">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="7405f-131">-WorkspaceName</span></span>
<span data-ttu-id="7405f-132">Çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="7405f-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="7405f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7405f-133">CommonParameters</span></span>
<span data-ttu-id="7405f-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7405f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7405f-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7405f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7405f-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7405f-136">INPUTS</span></span>

### <span data-ttu-id="7405f-137">Microsoft. Azure. PowerShell. cmdlet. Veriricks. model. ıdatabricksıdentity</span><span class="sxs-lookup"><span data-stu-id="7405f-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="7405f-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7405f-138">OUTPUTS</span></span>

### <span data-ttu-id="7405f-139">Microsoft. Azure. PowerShell. cmdlet. veriricks. modeller. Api20180401. ıvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="7405f-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="7405f-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7405f-140">NOTES</span></span>

<span data-ttu-id="7405f-141">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="7405f-141">ALIASES</span></span>

<span data-ttu-id="7405f-142">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="7405f-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7405f-143">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7405f-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7405f-144">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7405f-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7405f-145">INPUTOBJECT <IDatabricksIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="7405f-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7405f-146">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="7405f-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7405f-147">`[PeeringName <String>]`: Çalışma alanı vNet eşlemesi adı.</span><span class="sxs-lookup"><span data-stu-id="7405f-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="7405f-148">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7405f-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7405f-149">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="7405f-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="7405f-150">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7405f-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7405f-151">`[WorkspaceName <String>]`: Çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="7405f-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="7405f-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7405f-152">RELATED LINKS</span></span>

