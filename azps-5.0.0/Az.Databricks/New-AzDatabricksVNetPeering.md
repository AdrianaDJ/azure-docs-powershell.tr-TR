---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
ms.openlocfilehash: f1af71bd2c05f2b1219a3ad7f1f09eb2f9560ad4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320217"
---
# <span data-ttu-id="5be6c-101">New-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="5be6c-101">New-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="5be6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5be6c-102">SYNOPSIS</span></span>
<span data-ttu-id="5be6c-103">Çalışma alanı için vNet eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5be6c-103">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="5be6c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5be6c-104">SYNTAX</span></span>

```
New-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-AllowVirtualNetworkAccess]
 [-DatabricksAddressSpacePrefix <String[]>] [-DatabricksVirtualNetworkId <String>]
 [-RemoteAddressSpacePrefix <String[]>] [-RemoteVirtualNetworkId <String>] [-UseRemoteGateway]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5be6c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5be6c-105">DESCRIPTION</span></span>
<span data-ttu-id="5be6c-106">Çalışma alanı için vNet eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5be6c-106">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="5be6c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5be6c-107">EXAMPLES</span></span>

### <span data-ttu-id="5be6c-108">Örnek 1: verieşleri için VNET eşlemesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="5be6c-108">Example 1: Create a vnet peering for databricks</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t01 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxxx-xxxx-xxx-xxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test01'

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="5be6c-109">Bu komut, verieşleri için VNET eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5be6c-109">This command creates a vnet peering for databricks.</span></span>

## <span data-ttu-id="5be6c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5be6c-110">PARAMETERS</span></span>

### <span data-ttu-id="5be6c-111">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="5be6c-111">-AllowForwardedTraffic</span></span>
<span data-ttu-id="5be6c-112">Yerel sanal ağdaki VM 'Ler 'den iletilen trafiğin uzak sanal ağda izin verilip verilmeyeceğini denetler.</span><span class="sxs-lookup"><span data-stu-id="5be6c-112">Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="5be6c-113">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="5be6c-113">-AllowGatewayTransit</span></span>
<span data-ttu-id="5be6c-114">Bu sanal ağa bağlanmak için uzak sanal ağda ağ geçidi bağlantıları kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5be6c-114">If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="5be6c-115">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="5be6c-115">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="5be6c-116">Yerel sanal ağ alanındaki VM 'Lerin uzak sanal ağ alanındaki VM 'Lere erişip erişemeyeceğini.</span><span class="sxs-lookup"><span data-stu-id="5be6c-116">Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="5be6c-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="5be6c-117">-AsJob</span></span>
<span data-ttu-id="5be6c-118">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="5be6c-118">Run the command as a job</span></span>

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

### <span data-ttu-id="5be6c-119">-DatabricksAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="5be6c-119">-DatabricksAddressSpacePrefix</span></span>
<span data-ttu-id="5be6c-120">CıDR gösteriminde bu sanal ağa ayrılan adres bloklarının listesi.</span><span class="sxs-lookup"><span data-stu-id="5be6c-120">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5be6c-121">-Veriricksvirtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="5be6c-121">-DatabricksVirtualNetworkId</span></span>
<span data-ttu-id="5be6c-122">Veriricks sanal ağının kimliği.</span><span class="sxs-lookup"><span data-stu-id="5be6c-122">The Id of the databricks virtual network.</span></span>

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

### <span data-ttu-id="5be6c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5be6c-123">-DefaultProfile</span></span>
<span data-ttu-id="5be6c-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5be6c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5be6c-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="5be6c-125">-Name</span></span>
<span data-ttu-id="5be6c-126">Çalışma alanı vNet eşlemesi adı.</span><span class="sxs-lookup"><span data-stu-id="5be6c-126">The name of the workspace vNet peering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5be6c-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5be6c-127">-NoWait</span></span>
<span data-ttu-id="5be6c-128">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="5be6c-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5be6c-129">-RemoteAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="5be6c-129">-RemoteAddressSpacePrefix</span></span>
<span data-ttu-id="5be6c-130">CıDR gösteriminde bu sanal ağa ayrılan adres bloklarının listesi.</span><span class="sxs-lookup"><span data-stu-id="5be6c-130">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5be6c-131">-Remotevirtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="5be6c-131">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="5be6c-132">Uzak sanal ağın kimliği.</span><span class="sxs-lookup"><span data-stu-id="5be6c-132">The Id of the remote virtual network.</span></span>

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

### <span data-ttu-id="5be6c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5be6c-133">-ResourceGroupName</span></span>
<span data-ttu-id="5be6c-134">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5be6c-134">The name of the resource group.</span></span>
<span data-ttu-id="5be6c-135">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="5be6c-135">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5be6c-136">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="5be6c-136">-SubscriptionId</span></span>
<span data-ttu-id="5be6c-137">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5be6c-137">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5be6c-138">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="5be6c-138">-UseRemoteGateway</span></span>
<span data-ttu-id="5be6c-139">Bu sanal ağda uzak ağ geçitleri kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5be6c-139">If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="5be6c-140">Bayrak true olarak ayarlanırsa, uzak eşte allowGatewayTransit aynı zamanda doğruysa, sanal ağ geçiş için uzak sanal ağın ağ geçitlerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="5be6c-140">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="5be6c-141">Bu bayrak true olarak ayarlanmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="5be6c-141">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="5be6c-142">Sanal ağda ağ geçidi varsa, bu bayrak ayarlanamaz.</span><span class="sxs-lookup"><span data-stu-id="5be6c-142">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="5be6c-143">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="5be6c-143">-WorkspaceName</span></span>
<span data-ttu-id="5be6c-144">Çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="5be6c-144">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5be6c-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="5be6c-145">-Confirm</span></span>
<span data-ttu-id="5be6c-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5be6c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5be6c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5be6c-147">-WhatIf</span></span>
<span data-ttu-id="5be6c-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5be6c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5be6c-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5be6c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5be6c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5be6c-150">CommonParameters</span></span>
<span data-ttu-id="5be6c-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5be6c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5be6c-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5be6c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5be6c-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5be6c-153">INPUTS</span></span>

## <span data-ttu-id="5be6c-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5be6c-154">OUTPUTS</span></span>

### <span data-ttu-id="5be6c-155">Microsoft. Azure. PowerShell. cmdlet. veriricks. modeller. Api20180401. ıvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="5be6c-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="5be6c-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5be6c-156">NOTES</span></span>

<span data-ttu-id="5be6c-157">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="5be6c-157">ALIASES</span></span>

## <span data-ttu-id="5be6c-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5be6c-158">RELATED LINKS</span></span>

