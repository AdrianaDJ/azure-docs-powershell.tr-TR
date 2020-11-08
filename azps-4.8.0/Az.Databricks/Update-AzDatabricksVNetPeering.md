---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
ms.openlocfilehash: d53b45b67aa0843ddbdd8c5b063ff9295661a495
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273632"
---
# <span data-ttu-id="e16d0-101">Update-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="e16d0-101">Update-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="e16d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e16d0-102">SYNOPSIS</span></span>
<span data-ttu-id="e16d0-103">Çalışma alanı için vNet eşliğini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="e16d0-103">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="e16d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e16d0-104">SYNTAX</span></span>

### <span data-ttu-id="e16d0-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e16d0-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic <Boolean>] [-AllowGatewayTransit <Boolean>]
 [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e16d0-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="e16d0-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-AllowForwardedTraffic <Boolean>]
 [-AllowGatewayTransit <Boolean>] [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e16d0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e16d0-107">DESCRIPTION</span></span>
<span data-ttu-id="e16d0-108">Çalışma alanı için vNet eşliğini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="e16d0-108">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="e16d0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e16d0-109">EXAMPLES</span></span>

### <span data-ttu-id="e16d0-110">Örnek 1: VNET eşliğini güncelleştirme Allowforwardedtrafiği</span><span class="sxs-lookup"><span data-stu-id="e16d0-110">Example 1: Update AllowForwardedTraffic of vnet peering</span></span>
```powershell
PS C:\> Update-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 -AllowForwardedTraffic $True

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="e16d0-111">Bu komut, VNET eşlemesi 'nin Allowforwardedtrafiği güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e16d0-111">This command updates AllowForwardedTraffic of vnet peering.</span></span>

### <span data-ttu-id="e16d0-112">Örnek 2: nesne tarafından VNET eşliğini güncelleştirme Allowforwardedtrafiği</span><span class="sxs-lookup"><span data-stu-id="e16d0-112">Example 2: Update AllowForwardedTraffic of vnet peering by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 | Update-AzDatabricksVNetPeering -AllowGatewayTransit $true

Name            Type
----            ----
vnetpeering-t01

```

<span data-ttu-id="e16d0-113">Bu komut, nesne tarafından VNET eşlemesi için Allowforwardedtrafiği güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e16d0-113">This command updates AllowForwardedTraffic of vnet peering by object.</span></span>

## <span data-ttu-id="e16d0-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e16d0-114">PARAMETERS</span></span>

### <span data-ttu-id="e16d0-115">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="e16d0-115">-AllowForwardedTraffic</span></span>
<span data-ttu-id="e16d0-116">[System. Management. Automation. SwitchParameter] yerel sanal ağdaki VM 'Ler 'den iletilen trafiğin uzak sanal ağda izin verilip verilmeyeceğini denetler.</span><span class="sxs-lookup"><span data-stu-id="e16d0-116">[System.Management.Automation.SwitchParameter] Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16d0-117">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="e16d0-117">-AllowGatewayTransit</span></span>
<span data-ttu-id="e16d0-118">[System. Management. Automation. SwitchParameter] uzak sanal ağ 'da bu sanal ağa bağlanmak için ağ geçidi bağlantıları kullanılıyorsa.</span><span class="sxs-lookup"><span data-stu-id="e16d0-118">[System.Management.Automation.SwitchParameter] If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16d0-119">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="e16d0-119">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="e16d0-120">[System. Management. Automation. SwitchParameter] yerel sanal ağ alanındaki VM 'Lerin uzak sanal ağ alanındaki VM 'Lere erişip erişemeyeceğini.</span><span class="sxs-lookup"><span data-stu-id="e16d0-120">[System.Management.Automation.SwitchParameter] Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16d0-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="e16d0-121">-AsJob</span></span>
<span data-ttu-id="e16d0-122">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="e16d0-122">Run the command as a job</span></span>

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

### <span data-ttu-id="e16d0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e16d0-123">-DefaultProfile</span></span>
<span data-ttu-id="e16d0-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e16d0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e16d0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e16d0-125">-InputObject</span></span>
<span data-ttu-id="e16d0-126">Kimlik parametresi.</span><span class="sxs-lookup"><span data-stu-id="e16d0-126">Identity parameter.</span></span>
<span data-ttu-id="e16d0-127">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e16d0-127">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e16d0-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="e16d0-128">-Name</span></span>
<span data-ttu-id="e16d0-129">Vneteşleme adı.</span><span class="sxs-lookup"><span data-stu-id="e16d0-129">The name of the VNetPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PeeringName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16d0-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e16d0-130">-NoWait</span></span>
<span data-ttu-id="e16d0-131">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="e16d0-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e16d0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e16d0-132">-ResourceGroupName</span></span>
<span data-ttu-id="e16d0-133">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e16d0-133">The name of the resource group.</span></span>
<span data-ttu-id="e16d0-134">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="e16d0-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e16d0-135">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="e16d0-135">-SubscriptionId</span></span>
<span data-ttu-id="e16d0-136">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e16d0-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e16d0-137">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="e16d0-137">-UseRemoteGateway</span></span>
<span data-ttu-id="e16d0-138">Bu sanal ağda uzak ağ geçitleri kullanılıyorsa [System. Management. Automation. SwitchParameter].</span><span class="sxs-lookup"><span data-stu-id="e16d0-138">[System.Management.Automation.SwitchParameter] If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="e16d0-139">Bayrak true olarak ayarlanırsa, uzak eşte allowGatewayTransit aynı zamanda doğruysa, sanal ağ geçiş için uzak sanal ağın ağ geçitlerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e16d0-139">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="e16d0-140">Bu bayrak true olarak ayarlanmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="e16d0-140">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="e16d0-141">Sanal ağda ağ geçidi varsa, bu bayrak ayarlanamaz.</span><span class="sxs-lookup"><span data-stu-id="e16d0-141">This flag cannot be set if virtual network already has a gateway.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16d0-142">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="e16d0-142">-WorkspaceName</span></span>
<span data-ttu-id="e16d0-143">Çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="e16d0-143">The name of the workspace.</span></span>

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

### <span data-ttu-id="e16d0-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="e16d0-144">-Confirm</span></span>
<span data-ttu-id="e16d0-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e16d0-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e16d0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e16d0-146">-WhatIf</span></span>
<span data-ttu-id="e16d0-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e16d0-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e16d0-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e16d0-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e16d0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e16d0-149">CommonParameters</span></span>
<span data-ttu-id="e16d0-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e16d0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e16d0-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e16d0-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e16d0-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e16d0-152">INPUTS</span></span>

### <span data-ttu-id="e16d0-153">Microsoft. Azure. PowerShell. cmdlet. Veriricks. model. ıdatabricksıdentity</span><span class="sxs-lookup"><span data-stu-id="e16d0-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="e16d0-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e16d0-154">OUTPUTS</span></span>

### <span data-ttu-id="e16d0-155">Microsoft. Azure. PowerShell. cmdlet. veriricks. modeller. Api20180401. ıvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="e16d0-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="e16d0-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e16d0-156">NOTES</span></span>

<span data-ttu-id="e16d0-157">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="e16d0-157">ALIASES</span></span>

<span data-ttu-id="e16d0-158">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="e16d0-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e16d0-159">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e16d0-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e16d0-160">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e16d0-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e16d0-161">INPUTOBJECT <IDatabricksIdentity> : IDENTITY parametresi.</span><span class="sxs-lookup"><span data-stu-id="e16d0-161">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="e16d0-162">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="e16d0-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e16d0-163">`[PeeringName <String>]`: Çalışma alanı vNet eşlemesi adı.</span><span class="sxs-lookup"><span data-stu-id="e16d0-163">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="e16d0-164">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e16d0-164">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e16d0-165">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="e16d0-165">The name is case insensitive.</span></span>
  - <span data-ttu-id="e16d0-166">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e16d0-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e16d0-167">`[WorkspaceName <String>]`: Çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="e16d0-167">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="e16d0-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e16d0-168">RELATED LINKS</span></span>

