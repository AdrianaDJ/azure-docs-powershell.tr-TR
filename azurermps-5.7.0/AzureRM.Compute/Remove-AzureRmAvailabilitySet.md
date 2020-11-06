---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
ms.openlocfilehash: 467b430232805da132b568918ac0a1ed7b6db5c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587613"
---
# <span data-ttu-id="e0e01-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e0e01-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="e0e01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0e01-102">SYNOPSIS</span></span>
<span data-ttu-id="e0e01-103">Azure 'dan bir kullanılabilirlik kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e0e01-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0e01-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0e01-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0e01-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0e01-105">DESCRIPTION</span></span>
<span data-ttu-id="e0e01-106">**Remove-AzureRmAvailabilitySet** cmdlet 'i Azure 'dan bir kullanılabilirlik kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e0e01-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="e0e01-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0e01-107">EXAMPLES</span></span>

### <span data-ttu-id="e0e01-108">Örnek 1: kullanılabilirlik kümesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="e0e01-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="e0e01-109">Bu komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki bir kullanılabilirlik kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e0e01-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="e0e01-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0e01-110">PARAMETERS</span></span>

### <span data-ttu-id="e0e01-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e0e01-111">-Force</span></span>
<span data-ttu-id="e0e01-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e0e01-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="e0e01-113">-Name</span></span>
<span data-ttu-id="e0e01-114">Kullanılabilirlik kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="e0e01-114">The availability set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0e01-115">-ResourceGroupName</span></span>
<span data-ttu-id="e0e01-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0e01-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="e0e01-117">-Confirm</span></span>
<span data-ttu-id="e0e01-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e0e01-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0e01-119">-WhatIf</span></span>
<span data-ttu-id="e0e01-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0e01-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e0e01-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e0e01-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e01-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0e01-122">CommonParameters</span></span>
<span data-ttu-id="e0e01-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0e01-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0e01-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0e01-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0e01-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0e01-125">INPUTS</span></span>

### <span data-ttu-id="e0e01-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e0e01-126">None</span></span>
<span data-ttu-id="e0e01-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e0e01-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e0e01-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0e01-128">OUTPUTS</span></span>

## <span data-ttu-id="e0e01-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0e01-129">NOTES</span></span>

## <span data-ttu-id="e0e01-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0e01-130">RELATED LINKS</span></span>

[<span data-ttu-id="e0e01-131">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e0e01-131">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="e0e01-132">Yeni-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e0e01-132">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


