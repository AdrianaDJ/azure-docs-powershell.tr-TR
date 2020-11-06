---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualWan.md
ms.openlocfilehash: 3f62cf755ac06efe9ed5f04a6657a36cfe612abe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588449"
---
# <span data-ttu-id="6ed25-101">Update-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6ed25-101">Update-AzureRmVirtualWan</span></span>

## <span data-ttu-id="6ed25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ed25-102">SYNOPSIS</span></span>
<span data-ttu-id="6ed25-103">Azure sanal WAN 'ı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6ed25-103">Updates an Azure Virtual WAN.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ed25-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ed25-104">SYNTAX</span></span>

### <span data-ttu-id="6ed25-105">ByVirtualWanName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6ed25-105">ByVirtualWanName (Default)</span></span>
```
Update-AzureRmVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ed25-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="6ed25-106">ByVirtualWanObject</span></span>
```
Update-AzureRmVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ed25-107">İ Virtualwanresourceıd</span><span class="sxs-lookup"><span data-stu-id="6ed25-107">ByVirtualWanResourceId</span></span>
```
Update-AzureRmVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ed25-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ed25-108">DESCRIPTION</span></span>
<span data-ttu-id="6ed25-109">Azure sanal WAN 'ı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6ed25-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="6ed25-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ed25-110">EXAMPLES</span></span>

### <span data-ttu-id="6ed25-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6ed25-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="6ed25-112">Yukarıdaki "Batı ABD" bölgesinde "testRG" kaynak grubu ve Azure 'daki bu kaynak grubunda bir Azure sanal WAN oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6ed25-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="6ed25-113">VirtualWan yeni özelliklerle güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="6ed25-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="6ed25-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ed25-114">PARAMETERS</span></span>

### <span data-ttu-id="6ed25-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="6ed25-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="6ed25-116">VirtualWan için dal trafiğine izin verin.</span><span class="sxs-lookup"><span data-stu-id="6ed25-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ed25-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="6ed25-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="6ed25-118">VirtualWan için VNET 'den VNET trafiğine izin verin.</span><span class="sxs-lookup"><span data-stu-id="6ed25-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ed25-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="6ed25-119">-AsJob</span></span>
<span data-ttu-id="6ed25-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6ed25-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ed25-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ed25-121">-DefaultProfile</span></span>
<span data-ttu-id="6ed25-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ed25-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ed25-123">-Force</span><span class="sxs-lookup"><span data-stu-id="6ed25-123">-Force</span></span>
<span data-ttu-id="6ed25-124">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="6ed25-124">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="6ed25-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ed25-125">-InputObject</span></span>
<span data-ttu-id="6ed25-126">Değiştirilecek sanal WAN nesnesi</span><span class="sxs-lookup"><span data-stu-id="6ed25-126">The virtual wan object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ed25-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="6ed25-127">-Name</span></span>
<span data-ttu-id="6ed25-128">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="6ed25-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ed25-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ed25-129">-ResourceGroupName</span></span>
<span data-ttu-id="6ed25-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6ed25-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ed25-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6ed25-131">-ResourceId</span></span>
<span data-ttu-id="6ed25-132">Sanal WAN için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="6ed25-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ed25-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="6ed25-133">-Tag</span></span>
<span data-ttu-id="6ed25-134">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="6ed25-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ed25-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="6ed25-135">-Confirm</span></span>
<span data-ttu-id="6ed25-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6ed25-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ed25-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ed25-137">-WhatIf</span></span>
<span data-ttu-id="6ed25-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ed25-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ed25-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6ed25-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ed25-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ed25-140">CommonParameters</span></span>
<span data-ttu-id="6ed25-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ed25-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ed25-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ed25-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ed25-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ed25-143">INPUTS</span></span>

### <span data-ttu-id="6ed25-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6ed25-144">System.String</span></span>

### <span data-ttu-id="6ed25-145">Microsoft. Azure. Commands. Network. model. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6ed25-145">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="6ed25-146">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6ed25-146">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6ed25-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ed25-147">OUTPUTS</span></span>

### <span data-ttu-id="6ed25-148">Microsoft. Azure. Commands. Network. model. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6ed25-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="6ed25-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ed25-149">NOTES</span></span>

## <span data-ttu-id="6ed25-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ed25-150">RELATED LINKS</span></span>
