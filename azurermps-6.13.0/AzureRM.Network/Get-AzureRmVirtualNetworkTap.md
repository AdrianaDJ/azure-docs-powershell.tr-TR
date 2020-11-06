---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: ff9ed8220cf2b30f2e652e207cb4d63db969a8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589496"
---
# <span data-ttu-id="1a7b5-101">Get-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1a7b5-101">Get-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="1a7b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a7b5-102">SYNOPSIS</span></span>
<span data-ttu-id="1a7b5-103">Sanal ağ 'a dokunun</span><span class="sxs-lookup"><span data-stu-id="1a7b5-103">Gets a virtual network tap</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a7b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a7b5-104">SYNTAX</span></span>

### <span data-ttu-id="1a7b5-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1a7b5-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmVirtualNetworkTap -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a7b5-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="1a7b5-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a7b5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a7b5-107">DESCRIPTION</span></span>
<span data-ttu-id="1a7b5-108">**Get-AzureRmVirtualNetworkTap** cmdlet 'ı bir Azure sanal ağına dokunun veya kaynak grubundaki Azure sanal ağ dokunuş listesine dokunun.</span><span class="sxs-lookup"><span data-stu-id="1a7b5-108">The **Get-AzureRmVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="1a7b5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a7b5-109">EXAMPLES</span></span>

### <span data-ttu-id="1a7b5-110">Örnek 1: sanal ağ alma</span><span class="sxs-lookup"><span data-stu-id="1a7b5-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\>Get-AzureRmVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="1a7b5-111">Bu komut, "ResourceGroup1" içinde verilen "VirtualTap1" için VirtualNetwork dokunma başvurusu alır.</span><span class="sxs-lookup"><span data-stu-id="1a7b5-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

## <span data-ttu-id="1a7b5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a7b5-112">PARAMETERS</span></span>

### <span data-ttu-id="1a7b5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a7b5-113">-DefaultProfile</span></span>
<span data-ttu-id="1a7b5-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1a7b5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a7b5-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="1a7b5-115">-Name</span></span>
<span data-ttu-id="1a7b5-116">Dokunun adı.</span><span class="sxs-lookup"><span data-stu-id="1a7b5-116">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a7b5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a7b5-117">-ResourceGroupName</span></span>
<span data-ttu-id="1a7b5-118">Sanal ağın kaynak grup adı dokunun.</span><span class="sxs-lookup"><span data-stu-id="1a7b5-118">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a7b5-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1a7b5-119">-ResourceId</span></span>
<span data-ttu-id="1a7b5-120">VirtualNetworkTap kaynağının RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1a7b5-120">ResourceId of the VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="1a7b5-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="1a7b5-121">-Confirm</span></span>
<span data-ttu-id="1a7b5-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1a7b5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a7b5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a7b5-123">-WhatIf</span></span>
<span data-ttu-id="1a7b5-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a7b5-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a7b5-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1a7b5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a7b5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a7b5-126">CommonParameters</span></span>
<span data-ttu-id="1a7b5-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a7b5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a7b5-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a7b5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a7b5-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a7b5-129">INPUTS</span></span>

### <span data-ttu-id="1a7b5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1a7b5-130">System.String</span></span>

## <span data-ttu-id="1a7b5-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a7b5-131">OUTPUTS</span></span>

### <span data-ttu-id="1a7b5-132">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1a7b5-132">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="1a7b5-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a7b5-133">NOTES</span></span>

## <span data-ttu-id="1a7b5-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a7b5-134">RELATED LINKS</span></span>
