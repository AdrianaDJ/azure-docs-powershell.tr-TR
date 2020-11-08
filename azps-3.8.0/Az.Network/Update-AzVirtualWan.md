---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: e93bcc320f14a8311a29c6be9824da16506ea499
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104739"
---
# <span data-ttu-id="c3061-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c3061-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="c3061-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3061-102">SYNOPSIS</span></span>
<span data-ttu-id="c3061-103">Azure sanal WAN 'ı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c3061-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="c3061-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3061-104">SYNTAX</span></span>

### <span data-ttu-id="c3061-105">ByVirtualWanName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c3061-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3061-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="c3061-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3061-107">İ Virtualwanresourceıd</span><span class="sxs-lookup"><span data-stu-id="c3061-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3061-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3061-108">DESCRIPTION</span></span>
<span data-ttu-id="c3061-109">Azure sanal WAN 'ı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c3061-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="c3061-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3061-110">EXAMPLES</span></span>

### <span data-ttu-id="c3061-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c3061-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="c3061-112">Yukarıdaki "Batı ABD" bölgesinde "testRG" kaynak grubu ve Azure 'daki bu kaynak grubunda bir Azure sanal WAN oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c3061-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="c3061-113">VirtualWan yeni özelliklerle güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c3061-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="c3061-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3061-114">PARAMETERS</span></span>

### <span data-ttu-id="c3061-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="c3061-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="c3061-116">VirtualWan için dal trafiğine izin verin.</span><span class="sxs-lookup"><span data-stu-id="c3061-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3061-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="c3061-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="c3061-118">VirtualWan için VNET 'den VNET trafiğine izin verin.</span><span class="sxs-lookup"><span data-stu-id="c3061-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3061-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="c3061-119">-AsJob</span></span>
<span data-ttu-id="c3061-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c3061-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3061-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3061-121">-DefaultProfile</span></span>
<span data-ttu-id="c3061-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c3061-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3061-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c3061-123">-Force</span></span>
<span data-ttu-id="c3061-124">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="c3061-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3061-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3061-125">-InputObject</span></span>
<span data-ttu-id="c3061-126">Değiştirilecek sanal WAN nesnesi</span><span class="sxs-lookup"><span data-stu-id="c3061-126">The virtual wan object to be modified</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3061-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="c3061-127">-Name</span></span>
<span data-ttu-id="c3061-128">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="c3061-128">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3061-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3061-129">-ResourceGroupName</span></span>
<span data-ttu-id="c3061-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c3061-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3061-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c3061-131">-ResourceId</span></span>
<span data-ttu-id="c3061-132">Sanal WAN için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="c3061-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3061-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c3061-133">-Tag</span></span>
<span data-ttu-id="c3061-134">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="c3061-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3061-135">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="c3061-135">-VirtualWANType</span></span>
<span data-ttu-id="c3061-136">Sanal WAN 'ın türü.</span><span class="sxs-lookup"><span data-stu-id="c3061-136">The type of the Virtual Wan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3061-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="c3061-137">-Confirm</span></span>
<span data-ttu-id="c3061-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c3061-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3061-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3061-139">-WhatIf</span></span>
<span data-ttu-id="c3061-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c3061-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3061-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c3061-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3061-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3061-142">CommonParameters</span></span>
<span data-ttu-id="c3061-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3061-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3061-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c3061-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3061-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3061-145">INPUTS</span></span>

### <span data-ttu-id="c3061-146">Microsoft. Azure. Commands. Network. model. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c3061-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="c3061-147">System. String</span><span class="sxs-lookup"><span data-stu-id="c3061-147">System.String</span></span>

## <span data-ttu-id="c3061-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3061-148">OUTPUTS</span></span>

### <span data-ttu-id="c3061-149">Microsoft. Azure. Commands. Network. model. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c3061-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="c3061-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3061-150">NOTES</span></span>

## <span data-ttu-id="c3061-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3061-151">RELATED LINKS</span></span>

[<span data-ttu-id="c3061-152">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c3061-152">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="c3061-153">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c3061-153">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="c3061-154">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c3061-154">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
