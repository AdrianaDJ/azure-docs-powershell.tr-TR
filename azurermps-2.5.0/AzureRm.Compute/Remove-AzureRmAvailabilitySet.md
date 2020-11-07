---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: cc8292940a252844c0aeabe820eec2e62055c954
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939769"
---
# <span data-ttu-id="0b110-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0b110-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="0b110-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b110-102">SYNOPSIS</span></span>
<span data-ttu-id="0b110-103">Azure 'dan bir kullanılabilirlik kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0b110-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b110-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b110-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b110-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b110-105">DESCRIPTION</span></span>
<span data-ttu-id="0b110-106">**Remove-AzureRmAvailabilitySet** cmdlet 'i Azure 'dan bir kullanılabilirlik kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0b110-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="0b110-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b110-107">EXAMPLES</span></span>

### <span data-ttu-id="0b110-108">Örnek 1: kullanılabilirlik kümesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="0b110-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="0b110-109">Bu komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki bir kullanılabilirlik kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0b110-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="0b110-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b110-110">PARAMETERS</span></span>

### <span data-ttu-id="0b110-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="0b110-111">-AsJob</span></span>
<span data-ttu-id="0b110-112">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="0b110-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0b110-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b110-113">-DefaultProfile</span></span>
<span data-ttu-id="0b110-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b110-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b110-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0b110-115">-Force</span></span>
<span data-ttu-id="0b110-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="0b110-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0b110-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="0b110-117">-Name</span></span>
<span data-ttu-id="0b110-118">Kullanılabilirlik kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="0b110-118">The availability set name.</span></span>

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

### <span data-ttu-id="0b110-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b110-119">-ResourceGroupName</span></span>
<span data-ttu-id="0b110-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b110-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0b110-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="0b110-121">-Confirm</span></span>
<span data-ttu-id="0b110-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0b110-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b110-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b110-123">-WhatIf</span></span>
<span data-ttu-id="0b110-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b110-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="0b110-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0b110-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b110-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b110-126">CommonParameters</span></span>
<span data-ttu-id="0b110-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b110-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b110-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b110-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b110-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b110-129">INPUTS</span></span>

### <span data-ttu-id="0b110-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0b110-130">None</span></span>
<span data-ttu-id="0b110-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="0b110-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0b110-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b110-132">OUTPUTS</span></span>

### <span data-ttu-id="0b110-133">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0b110-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0b110-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b110-134">NOTES</span></span>

## <span data-ttu-id="0b110-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b110-135">RELATED LINKS</span></span>

[<span data-ttu-id="0b110-136">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0b110-136">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="0b110-137">Yeni-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0b110-137">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


