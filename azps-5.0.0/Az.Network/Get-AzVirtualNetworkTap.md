---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: dc6ca5c41e5f819c8f1db3d0c601b48273e3d78e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275978"
---
# <span data-ttu-id="448c9-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="448c9-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="448c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="448c9-102">SYNOPSIS</span></span>
<span data-ttu-id="448c9-103">Sanal ağ 'a dokunun</span><span class="sxs-lookup"><span data-stu-id="448c9-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="448c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="448c9-104">SYNTAX</span></span>

### <span data-ttu-id="448c9-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="448c9-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="448c9-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="448c9-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="448c9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="448c9-107">DESCRIPTION</span></span>
<span data-ttu-id="448c9-108">**Get-AzVirtualNetworkTap** cmdlet 'ı bir Azure sanal ağına dokunun veya kaynak grubundaki Azure sanal ağ dokunuş listesine dokunun.</span><span class="sxs-lookup"><span data-stu-id="448c9-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="448c9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="448c9-109">EXAMPLES</span></span>

### <span data-ttu-id="448c9-110">Örnek 1: sanal ağ alma</span><span class="sxs-lookup"><span data-stu-id="448c9-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="448c9-111">Bu komut, "ResourceGroup1" içinde verilen "VirtualTap1" için VirtualNetwork dokunma başvurusu alır.</span><span class="sxs-lookup"><span data-stu-id="448c9-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="448c9-112">Örnek 2: filtreleme kullanarak tüm sanal ağ dokunuş</span><span class="sxs-lookup"><span data-stu-id="448c9-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="448c9-113">Bu komut, "VirtualTap" ile başlayan tüm VirtualNetwork dokunma başvurularını alır.</span><span class="sxs-lookup"><span data-stu-id="448c9-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="448c9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="448c9-114">PARAMETERS</span></span>

### <span data-ttu-id="448c9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="448c9-115">-DefaultProfile</span></span>
<span data-ttu-id="448c9-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="448c9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="448c9-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="448c9-117">-Name</span></span>
<span data-ttu-id="448c9-118">Dokunun adı.</span><span class="sxs-lookup"><span data-stu-id="448c9-118">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="448c9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="448c9-119">-ResourceGroupName</span></span>
<span data-ttu-id="448c9-120">Sanal ağın kaynak grup adı dokunun.</span><span class="sxs-lookup"><span data-stu-id="448c9-120">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="448c9-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="448c9-121">-ResourceId</span></span>
<span data-ttu-id="448c9-122">VirtualNetworkTap kaynağının RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="448c9-122">ResourceId of the VirtualNetworkTap resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="448c9-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="448c9-123">-Confirm</span></span>
<span data-ttu-id="448c9-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="448c9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="448c9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="448c9-125">-WhatIf</span></span>
<span data-ttu-id="448c9-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="448c9-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="448c9-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="448c9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="448c9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="448c9-128">CommonParameters</span></span>
<span data-ttu-id="448c9-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="448c9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="448c9-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="448c9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="448c9-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="448c9-131">INPUTS</span></span>

### <span data-ttu-id="448c9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="448c9-132">System.String</span></span>

## <span data-ttu-id="448c9-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="448c9-133">OUTPUTS</span></span>

### <span data-ttu-id="448c9-134">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="448c9-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="448c9-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="448c9-135">NOTES</span></span>

## <span data-ttu-id="448c9-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="448c9-136">RELATED LINKS</span></span>

[<span data-ttu-id="448c9-137">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="448c9-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="448c9-138">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="448c9-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="448c9-139">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="448c9-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
