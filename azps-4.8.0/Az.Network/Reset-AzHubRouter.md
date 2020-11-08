---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azhubrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
ms.openlocfilehash: 039d37f9d9dd7b5af026b7ce2a87113513949b67
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267002"
---
# <span data-ttu-id="a99fd-101">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="a99fd-101">Reset-AzHubRouter</span></span>

## <span data-ttu-id="a99fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a99fd-102">SYNOPSIS</span></span>
<span data-ttu-id="a99fd-103">VirtualHub kaynağının RoutingState durumunu sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="a99fd-103">Resets the RoutingState of a VirtualHub resource.</span></span>

## <span data-ttu-id="a99fd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a99fd-104">SYNTAX</span></span>

### <span data-ttu-id="a99fd-105">ByVirtualHubName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a99fd-105">ByVirtualHubName (Default)</span></span>
```
Reset-AzHubRouter -ResourceGroupName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a99fd-106">Byvirtualhubresourceıd</span><span class="sxs-lookup"><span data-stu-id="a99fd-106">ByVirtualHubResourceId</span></span>
```
Reset-AzHubRouter -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a99fd-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="a99fd-107">ByVirtualHubObject</span></span>
```
Reset-AzHubRouter -InputObject <PSVirtualHub> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a99fd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a99fd-108">DESCRIPTION</span></span>
<span data-ttu-id="a99fd-109">Yalnızca sanal hub 'ın yönlendirme durumu sağlanmadıysa, var olan VirtualHub kaynağının yönlendirme durumunu sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="a99fd-109">Resets the Routing State of an existing VirtualHub resource only if the Routing State of the virtual hub is not Provisioned.</span></span>

## <span data-ttu-id="a99fd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a99fd-110">EXAMPLES</span></span>

### <span data-ttu-id="a99fd-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a99fd-111">Example 1</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="a99fd-112">Sanal hub 'ın yönlendirme durumunu, ResourceGroupName ve ResourceName kullanarak sıfırlayın.</span><span class="sxs-lookup"><span data-stu-id="a99fd-112">Reset the routing state of the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="a99fd-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a99fd-113">Example 2</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceId "/subscriptions/testSub/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub"
```

<span data-ttu-id="a99fd-114">Sanal hub 'ın RESOURCEID 'sini kullanarak yönlendirme durumunu sıfırlayın.</span><span class="sxs-lookup"><span data-stu-id="a99fd-114">Reset the routing state of the virtual hub using its ResourceId.</span></span>

### <span data-ttu-id="a99fd-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="a99fd-115">Example 3</span></span>

```powershell
PS C:\> Reset-AzHubRouter -InputObject $virtualHub
```

<span data-ttu-id="a99fd-116">Bir giriş nesnesi kullanarak sanal hub 'ın yönlendirme durumunu sıfırlayın.</span><span class="sxs-lookup"><span data-stu-id="a99fd-116">Reset the routing state of the virtual hub using an input object.</span></span> <span data-ttu-id="a99fd-117">Giriş nesnesi PSVirtualHub türünde.</span><span class="sxs-lookup"><span data-stu-id="a99fd-117">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="a99fd-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="a99fd-118">Example 4</span></span>

```powershell
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Reset-AzHubRouter
```

<span data-ttu-id="a99fd-119">Var olan bir sanal hub nesnesinin alınıp sıfırlanması için giriş nesnesi olarak sıfırlanması gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="a99fd-119">An existing virtual hub object can be retrieved and then passed as input object to Reset-AzHubRouter.</span></span>

## <span data-ttu-id="a99fd-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a99fd-120">PARAMETERS</span></span>

### <span data-ttu-id="a99fd-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="a99fd-121">-AsJob</span></span>
<span data-ttu-id="a99fd-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a99fd-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a99fd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a99fd-123">-DefaultProfile</span></span>
<span data-ttu-id="a99fd-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a99fd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99fd-125">-Force</span><span class="sxs-lookup"><span data-stu-id="a99fd-125">-Force</span></span>
<span data-ttu-id="a99fd-126">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="a99fd-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a99fd-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a99fd-127">-InputObject</span></span>
<span data-ttu-id="a99fd-128">Değiştirilecek sanal hub nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a99fd-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a99fd-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="a99fd-129">-Name</span></span>
<span data-ttu-id="a99fd-130">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="a99fd-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99fd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a99fd-131">-ResourceGroupName</span></span>
<span data-ttu-id="a99fd-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a99fd-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99fd-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a99fd-133">-ResourceId</span></span>
<span data-ttu-id="a99fd-134">Değiştirilecek sanal hub 'ın kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="a99fd-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a99fd-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="a99fd-135">-Confirm</span></span>
<span data-ttu-id="a99fd-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a99fd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a99fd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a99fd-137">-WhatIf</span></span>
<span data-ttu-id="a99fd-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a99fd-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a99fd-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a99fd-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a99fd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a99fd-140">CommonParameters</span></span>
<span data-ttu-id="a99fd-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a99fd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a99fd-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a99fd-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a99fd-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a99fd-143">INPUTS</span></span>

### <span data-ttu-id="a99fd-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a99fd-144">System.String</span></span>

### <span data-ttu-id="a99fd-145">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a99fd-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="a99fd-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a99fd-146">OUTPUTS</span></span>

### <span data-ttu-id="a99fd-147">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a99fd-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="a99fd-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a99fd-148">NOTES</span></span>

## <span data-ttu-id="a99fd-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a99fd-149">RELATED LINKS</span></span>

[<span data-ttu-id="a99fd-150">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a99fd-150">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)
