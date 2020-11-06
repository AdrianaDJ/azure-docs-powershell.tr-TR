---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualWan.md
ms.openlocfilehash: 1ff9eb4307c4419dd303d74f7528a8ee0d50bdf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589426"
---
# <span data-ttu-id="cde36-101">Remove-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="cde36-101">Remove-AzureRmVirtualWan</span></span>

## <span data-ttu-id="cde36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cde36-102">SYNOPSIS</span></span>
<span data-ttu-id="cde36-103">Azure sanal WAN 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cde36-103">Removes an Azure Virtual WAN.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cde36-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cde36-104">SYNTAX</span></span>

### <span data-ttu-id="cde36-105">ByVirtualWanName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cde36-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzureRmVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cde36-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="cde36-106">ByVirtualWanObject</span></span>
```
Remove-AzureRmVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cde36-107">İ Virtualwanresourceıd</span><span class="sxs-lookup"><span data-stu-id="cde36-107">ByVirtualWanResourceId</span></span>
```
Remove-AzureRmVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cde36-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cde36-108">DESCRIPTION</span></span>
<span data-ttu-id="cde36-109">Azure sanal WAN 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cde36-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="cde36-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cde36-110">EXAMPLES</span></span>

### <span data-ttu-id="cde36-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cde36-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzureRmVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzureRmVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="cde36-112">Bu örnekte, kaynak grubunda sanal bir WAN oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="cde36-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="cde36-113">Sanal WAN silinirken istemi bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="cde36-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="cde36-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="cde36-114">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzureRmVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzureRmVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="cde36-115">Bu örnekte, kaynak grubunda sanal bir WAN oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="cde36-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="cde36-116">Bu silme işlemi, yeni-AzureRmVirtualWan tarafından döndürülen sanal WAN nesnesini kullanıyor.</span><span class="sxs-lookup"><span data-stu-id="cde36-116">This deletion happens using the virtual wan object returned by New-AzureRmVirtualWan.</span></span>
<span data-ttu-id="cde36-117">Sanal WAN silinirken istemi bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="cde36-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="cde36-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="cde36-118">Example 3</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzureRmVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzureRmVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="cde36-119">Bu örnekte, kaynak grubunda sanal bir WAN oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="cde36-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="cde36-120">Bu silme işlemi, yeni-AzureRmVirtualWan tarafından döndürülen sanal WAN kaynak kimliğini kullanarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="cde36-120">This deletion happens using the virtual wan resource id returned by New-AzureRmVirtualWan.</span></span>
<span data-ttu-id="cde36-121">Sanal WAN silinirken istemi bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="cde36-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="cde36-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cde36-122">PARAMETERS</span></span>

### <span data-ttu-id="cde36-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cde36-123">-DefaultProfile</span></span>
<span data-ttu-id="cde36-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cde36-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cde36-125">-Force</span><span class="sxs-lookup"><span data-stu-id="cde36-125">-Force</span></span>
<span data-ttu-id="cde36-126">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="cde36-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cde36-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cde36-127">-InputObject</span></span>
<span data-ttu-id="cde36-128">Silinecek sanal WAN nesnesi.</span><span class="sxs-lookup"><span data-stu-id="cde36-128">The virtual wan object to be deleted.</span></span>

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

### <span data-ttu-id="cde36-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="cde36-129">-Name</span></span>
<span data-ttu-id="cde36-130">Sanal WAN adı.</span><span class="sxs-lookup"><span data-stu-id="cde36-130">The virtual wan name.</span></span>

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

### <span data-ttu-id="cde36-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cde36-131">-PassThru</span></span>
<span data-ttu-id="cde36-132">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="cde36-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cde36-133">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="cde36-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cde36-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cde36-134">-ResourceGroupName</span></span>
<span data-ttu-id="cde36-135">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="cde36-135">The resource group name.</span></span>

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

### <span data-ttu-id="cde36-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cde36-136">-ResourceId</span></span>
<span data-ttu-id="cde36-137">Silinecek sanal WAN için Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cde36-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

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

### <span data-ttu-id="cde36-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="cde36-138">-Confirm</span></span>
<span data-ttu-id="cde36-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cde36-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cde36-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cde36-140">-WhatIf</span></span>
<span data-ttu-id="cde36-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cde36-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cde36-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cde36-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cde36-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cde36-143">CommonParameters</span></span>
<span data-ttu-id="cde36-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cde36-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cde36-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cde36-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cde36-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cde36-146">INPUTS</span></span>

### <span data-ttu-id="cde36-147">Microsoft. Azure. Commands. Network. model. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="cde36-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="cde36-148">System. String</span><span class="sxs-lookup"><span data-stu-id="cde36-148">System.String</span></span>

## <span data-ttu-id="cde36-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cde36-149">OUTPUTS</span></span>

### <span data-ttu-id="cde36-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cde36-150">System.Boolean</span></span>

## <span data-ttu-id="cde36-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cde36-151">NOTES</span></span>

## <span data-ttu-id="cde36-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cde36-152">RELATED LINKS</span></span>
