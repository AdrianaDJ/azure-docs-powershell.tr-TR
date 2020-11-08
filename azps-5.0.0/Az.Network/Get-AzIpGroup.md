---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
ms.openlocfilehash: 11c5e3ff2d8ee548917de7a94b1a592ae4cce52b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279498"
---
# <span data-ttu-id="d3b04-101">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d3b04-101">Get-AzIpGroup</span></span>

## <span data-ttu-id="d3b04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3b04-102">SYNOPSIS</span></span>
<span data-ttu-id="d3b04-103">Azure ıpgroup alın</span><span class="sxs-lookup"><span data-stu-id="d3b04-103">Get an Azure IpGroup</span></span>

## <span data-ttu-id="d3b04-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3b04-104">SYNTAX</span></span>

### <span data-ttu-id="d3b04-105">Ipgroupnameparameterset</span><span class="sxs-lookup"><span data-stu-id="d3b04-105">IpGroupNameParameterSet</span></span>
```
Get-AzIpGroup -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3b04-106">Ipgroupresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d3b04-106">IpGroupResourceIdParameterSet</span></span>
```
Get-AzIpGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3b04-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3b04-107">DESCRIPTION</span></span>
<span data-ttu-id="d3b04-108">**Get-Azıpgroup** cmdlet 'ı bir Azure ıpgroup alır</span><span class="sxs-lookup"><span data-stu-id="d3b04-108">The **Get-AzIpGroup** cmdlet gets an Azure IpGroup</span></span>

## <span data-ttu-id="d3b04-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3b04-109">EXAMPLES</span></span>

### <span data-ttu-id="d3b04-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d3b04-110">Example 1</span></span>
```powershell
Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="d3b04-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d3b04-111">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Get-AzIpGroup -ResourceId $ipGroupId
```

## <span data-ttu-id="d3b04-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3b04-112">PARAMETERS</span></span>

### <span data-ttu-id="d3b04-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3b04-113">-DefaultProfile</span></span>
<span data-ttu-id="d3b04-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d3b04-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3b04-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d3b04-115">-Name</span></span>
<span data-ttu-id="d3b04-116">Ipgroup 'un adı.</span><span class="sxs-lookup"><span data-stu-id="d3b04-116">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b04-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3b04-117">-ResourceGroupName</span></span>
<span data-ttu-id="d3b04-118">Ipgroup 'un kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d3b04-118">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b04-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d3b04-119">-ResourceId</span></span>
<span data-ttu-id="d3b04-120">Ipgroup 'un RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="d3b04-120">ResourceId of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b04-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3b04-121">CommonParameters</span></span>
<span data-ttu-id="d3b04-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3b04-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3b04-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d3b04-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3b04-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3b04-124">INPUTS</span></span>

### <span data-ttu-id="d3b04-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d3b04-125">System.String</span></span>

## <span data-ttu-id="d3b04-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3b04-126">OUTPUTS</span></span>

### <span data-ttu-id="d3b04-127">Microsoft. Azure. Commands. Network. model. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="d3b04-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="d3b04-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3b04-128">NOTES</span></span>

## <span data-ttu-id="d3b04-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3b04-129">RELATED LINKS</span></span>
