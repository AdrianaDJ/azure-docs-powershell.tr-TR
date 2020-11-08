---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
ms.openlocfilehash: 4d817dcabe73972b3a8f21de5b9b0906d7a95cc2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108838"
---
# <span data-ttu-id="d7868-101">Set-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="d7868-101">Set-AzIpAllocation</span></span>

## <span data-ttu-id="d7868-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7868-102">SYNOPSIS</span></span>
<span data-ttu-id="d7868-103">Değiştirilmiş bir IP ayırması kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d7868-103">Saves a modified IpAllocation.</span></span>

## <span data-ttu-id="d7868-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7868-104">SYNTAX</span></span>

### <span data-ttu-id="d7868-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7868-105">SetByNameParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-IpAllocationTag <Hashtable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7868-106">Setbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d7868-106">SetByResourceIdParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceId] <String> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7868-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7868-107">SetByInputObjectParameterSet</span></span>
```
Set-AzIpAllocation [-InputObject] <PSIpAllocation> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7868-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7868-108">DESCRIPTION</span></span>
<span data-ttu-id="d7868-109">**Set-Azıpallocation** cmdlet 'ı bir Azure IP ayırmasını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="d7868-109">The **Set-AzIpAllocation** cmdlet updates an Azure IpAllocation</span></span>

## <span data-ttu-id="d7868-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7868-110">EXAMPLES</span></span>

### <span data-ttu-id="d7868-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d7868-111">Example 1</span></span>
```powershell
Set-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'  -IpAllocationTag @{"VnetId"="vnet1"}  -Tag @{"TestTag"="TestValue"}
```

## <span data-ttu-id="d7868-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7868-112">PARAMETERS</span></span>

### <span data-ttu-id="d7868-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="d7868-113">-AsJob</span></span>
<span data-ttu-id="d7868-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d7868-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7868-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7868-115">-DefaultProfile</span></span>
<span data-ttu-id="d7868-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d7868-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7868-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7868-117">-InputObject</span></span>
<span data-ttu-id="d7868-118">Ipallocation</span><span class="sxs-lookup"><span data-stu-id="d7868-118">The IpAllocation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation
Parameter Sets: SetByInputObjectParameterSet
Aliases: IpAllocation

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7868-119">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="d7868-119">-IpAllocationTag</span></span>
<span data-ttu-id="d7868-120">IP ayırmanın ayırma etiketleri</span><span class="sxs-lookup"><span data-stu-id="d7868-120">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="d7868-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="d7868-121">-Name</span></span>
<span data-ttu-id="d7868-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="d7868-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7868-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7868-123">-ResourceGroupName</span></span>
<span data-ttu-id="d7868-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d7868-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7868-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d7868-125">-ResourceId</span></span>
<span data-ttu-id="d7868-126">IP ayırma kimliği</span><span class="sxs-lookup"><span data-stu-id="d7868-126">IpAllocation Id</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: IpAllocationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7868-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d7868-127">-Tag</span></span>
<span data-ttu-id="d7868-128">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="d7868-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d7868-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7868-129">CommonParameters</span></span>
<span data-ttu-id="d7868-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7868-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7868-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d7868-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7868-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7868-132">INPUTS</span></span>

### <span data-ttu-id="d7868-133">Microsoft. Azure. Commands. Network. model. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="d7868-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="d7868-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7868-134">OUTPUTS</span></span>

### <span data-ttu-id="d7868-135">Microsoft. Azure. Commands. Network. model. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="d7868-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="d7868-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7868-136">NOTES</span></span>

## <span data-ttu-id="d7868-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7868-137">RELATED LINKS</span></span>
