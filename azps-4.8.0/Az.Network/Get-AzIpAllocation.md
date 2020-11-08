---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: 89a0276a94ffa2729c5803a017e297ff05e84534
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274141"
---
# <span data-ttu-id="f55d1-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="f55d1-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="f55d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f55d1-102">SYNOPSIS</span></span>
<span data-ttu-id="f55d1-103">Bir Azure IP ayırması alır.</span><span class="sxs-lookup"><span data-stu-id="f55d1-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="f55d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f55d1-104">SYNTAX</span></span>

### <span data-ttu-id="f55d1-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f55d1-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f55d1-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="f55d1-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f55d1-107">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f55d1-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f55d1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f55d1-108">DESCRIPTION</span></span>
<span data-ttu-id="f55d1-109">**Get-Azıpallocation** cmdlet 'ı bir Azure IP ayırması alır</span><span class="sxs-lookup"><span data-stu-id="f55d1-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="f55d1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f55d1-110">EXAMPLES</span></span>

### <span data-ttu-id="f55d1-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f55d1-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="f55d1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f55d1-112">PARAMETERS</span></span>

### <span data-ttu-id="f55d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f55d1-113">-DefaultProfile</span></span>
<span data-ttu-id="f55d1-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f55d1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f55d1-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="f55d1-115">-Name</span></span>
<span data-ttu-id="f55d1-116">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="f55d1-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55d1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f55d1-117">-ResourceGroupName</span></span>
<span data-ttu-id="f55d1-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f55d1-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55d1-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f55d1-119">-ResourceId</span></span>
<span data-ttu-id="f55d1-120">IP ayırma kimliği</span><span class="sxs-lookup"><span data-stu-id="f55d1-120">IpAllocation Id</span></span>

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

### <span data-ttu-id="f55d1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f55d1-121">CommonParameters</span></span>
<span data-ttu-id="f55d1-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f55d1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f55d1-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f55d1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f55d1-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f55d1-124">INPUTS</span></span>

### <span data-ttu-id="f55d1-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f55d1-125">System.String</span></span>

## <span data-ttu-id="f55d1-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f55d1-126">OUTPUTS</span></span>

### <span data-ttu-id="f55d1-127">Microsoft. Azure. Commands. Network. model. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="f55d1-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="f55d1-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f55d1-128">NOTES</span></span>

## <span data-ttu-id="f55d1-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f55d1-129">RELATED LINKS</span></span>
