---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
ms.openlocfilehash: 6ae61090f98cbb9929cc5ad1b2745fbf88f21a2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323803"
---
# <span data-ttu-id="7fccf-101">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7fccf-101">New-AzIpGroup</span></span>

## <span data-ttu-id="7fccf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fccf-102">SYNOPSIS</span></span>
<span data-ttu-id="7fccf-103">Azure ıpgroup oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7fccf-103">Creates an Azure IpGroup.</span></span>

## <span data-ttu-id="7fccf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7fccf-104">SYNTAX</span></span>

```
New-AzIpGroup -Name <String> -ResourceGroupName <String> [-IpAddress <String[]>] -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7fccf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7fccf-105">DESCRIPTION</span></span>
<span data-ttu-id="7fccf-106">**New-Azıpgroup** cmdlet 'ı bir Azure ıpgroup oluşturur</span><span class="sxs-lookup"><span data-stu-id="7fccf-106">The **New-AzIpGroup** cmdlet creates an Azure IpGroup</span></span>

## <span data-ttu-id="7fccf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7fccf-107">EXAMPLES</span></span>

### <span data-ttu-id="7fccf-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7fccf-108">Example 1</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US'
```

### <span data-ttu-id="7fccf-109">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7fccf-109">Example 2</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US' -IpAddress 10.0.0.0/24,11.9.0.0/24
```

## <span data-ttu-id="7fccf-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7fccf-110">PARAMETERS</span></span>

### <span data-ttu-id="7fccf-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="7fccf-111">-AsJob</span></span>
<span data-ttu-id="7fccf-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7fccf-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7fccf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fccf-113">-DefaultProfile</span></span>
<span data-ttu-id="7fccf-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7fccf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fccf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7fccf-115">-Force</span></span>
<span data-ttu-id="7fccf-116">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="7fccf-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7fccf-117">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="7fccf-117">-IpAddress</span></span>
<span data-ttu-id="7fccf-118">Ipgroup 'ta tanımlanan IP adresleri</span><span class="sxs-lookup"><span data-stu-id="7fccf-118">IpAddresses defined in the IpGroup</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fccf-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="7fccf-119">-Location</span></span>
<span data-ttu-id="7fccf-120">Konum.</span><span class="sxs-lookup"><span data-stu-id="7fccf-120">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fccf-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="7fccf-121">-Name</span></span>
<span data-ttu-id="7fccf-122">Ipgroup 'un adı.</span><span class="sxs-lookup"><span data-stu-id="7fccf-122">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fccf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fccf-123">-ResourceGroupName</span></span>
<span data-ttu-id="7fccf-124">Ipgroup 'un kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7fccf-124">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fccf-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7fccf-125">-Tag</span></span>
<span data-ttu-id="7fccf-126">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="7fccf-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fccf-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="7fccf-127">-Confirm</span></span>
<span data-ttu-id="7fccf-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7fccf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fccf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fccf-129">-WhatIf</span></span>
<span data-ttu-id="7fccf-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7fccf-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fccf-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7fccf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fccf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fccf-132">CommonParameters</span></span>
<span data-ttu-id="7fccf-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7fccf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fccf-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7fccf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fccf-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7fccf-135">INPUTS</span></span>

### <span data-ttu-id="7fccf-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7fccf-136">System.String</span></span>

### <span data-ttu-id="7fccf-137">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7fccf-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="7fccf-138">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7fccf-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7fccf-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7fccf-139">OUTPUTS</span></span>

### <span data-ttu-id="7fccf-140">Microsoft. Azure. Commands. Network. model. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="7fccf-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="7fccf-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7fccf-141">NOTES</span></span>

## <span data-ttu-id="7fccf-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7fccf-142">RELATED LINKS</span></span>
