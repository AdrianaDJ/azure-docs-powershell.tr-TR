---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: 7a81ce555ed99de1504dc0625c0c83cdab6ab881
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109439"
---
# <span data-ttu-id="ea412-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="ea412-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="ea412-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea412-102">SYNOPSIS</span></span>
<span data-ttu-id="ea412-103">Azure ıpallocation 'i siler.</span><span class="sxs-lookup"><span data-stu-id="ea412-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="ea412-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea412-104">SYNTAX</span></span>

### <span data-ttu-id="ea412-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea412-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea412-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea412-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea412-107">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ea412-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea412-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea412-108">DESCRIPTION</span></span>
<span data-ttu-id="ea412-109">**Remove-Azıpallocation** cmdlet 'ı bir Azure ıpallocation 'i siler</span><span class="sxs-lookup"><span data-stu-id="ea412-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="ea412-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea412-110">EXAMPLES</span></span>

### <span data-ttu-id="ea412-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ea412-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="ea412-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea412-112">PARAMETERS</span></span>

### <span data-ttu-id="ea412-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="ea412-113">-AsJob</span></span>
<span data-ttu-id="ea412-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ea412-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea412-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea412-115">-DefaultProfile</span></span>
<span data-ttu-id="ea412-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ea412-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea412-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ea412-117">-Force</span></span>
<span data-ttu-id="ea412-118">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="ea412-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ea412-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea412-119">-InputObject</span></span>
<span data-ttu-id="ea412-120">{{Fill InputObject açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="ea412-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTopLevelResource
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea412-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="ea412-121">-Name</span></span>
<span data-ttu-id="ea412-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="ea412-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea412-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ea412-123">-PassThru</span></span>
<span data-ttu-id="ea412-124">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="ea412-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ea412-125">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="ea412-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ea412-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea412-126">-ResourceGroupName</span></span>
<span data-ttu-id="ea412-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ea412-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea412-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ea412-128">-ResourceId</span></span>
<span data-ttu-id="ea412-129">IP ayırma kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="ea412-129">IpAllocation resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea412-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="ea412-130">-Confirm</span></span>
<span data-ttu-id="ea412-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ea412-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea412-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea412-132">-WhatIf</span></span>
<span data-ttu-id="ea412-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ea412-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea412-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ea412-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea412-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea412-135">CommonParameters</span></span>
<span data-ttu-id="ea412-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea412-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea412-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ea412-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea412-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea412-138">INPUTS</span></span>

### <span data-ttu-id="ea412-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ea412-139">System.String</span></span>

## <span data-ttu-id="ea412-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea412-140">OUTPUTS</span></span>

### <span data-ttu-id="ea412-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea412-141">System.Boolean</span></span>

## <span data-ttu-id="ea412-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea412-142">NOTES</span></span>

## <span data-ttu-id="ea412-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea412-143">RELATED LINKS</span></span>
