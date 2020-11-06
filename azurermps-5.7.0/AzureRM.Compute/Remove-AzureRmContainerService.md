---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
ms.openlocfilehash: da4f9846f8fceaaecc6d4385374f6525d3243e3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587612"
---
# <span data-ttu-id="9975a-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9975a-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="9975a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9975a-102">SYNOPSIS</span></span>
<span data-ttu-id="9975a-103">Kapsayıcı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9975a-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9975a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9975a-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9975a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9975a-105">DESCRIPTION</span></span>
<span data-ttu-id="9975a-106">**Remove-AzureRmContainerService** cmdlet 'i Azure hesabınızdan bir kapsayıcı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9975a-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="9975a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9975a-107">EXAMPLES</span></span>

### <span data-ttu-id="9975a-108">Örnek 1: kapsayıcı hizmeti kaldırma</span><span class="sxs-lookup"><span data-stu-id="9975a-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="9975a-109">Bu komut, CSResourceGroup17 adlı kapsayıcı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9975a-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="9975a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9975a-110">PARAMETERS</span></span>

### <span data-ttu-id="9975a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="9975a-111">-Force</span></span>
<span data-ttu-id="9975a-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="9975a-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9975a-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="9975a-113">-Name</span></span>
<span data-ttu-id="9975a-114">Bu cmdlet 'in kaldırdığı kapsayıcı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9975a-114">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9975a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9975a-115">-ResourceGroupName</span></span>
<span data-ttu-id="9975a-116">Bu cmdlet 'in kaldırdığı kapsayıcı hizmetin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9975a-116">Specifies the resource group of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9975a-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="9975a-117">-Confirm</span></span>
<span data-ttu-id="9975a-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9975a-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="9975a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9975a-119">-WhatIf</span></span>
<span data-ttu-id="9975a-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9975a-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9975a-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9975a-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="9975a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9975a-122">CommonParameters</span></span>
<span data-ttu-id="9975a-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9975a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9975a-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9975a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9975a-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9975a-125">INPUTS</span></span>

### <span data-ttu-id="9975a-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9975a-126">None</span></span>
<span data-ttu-id="9975a-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="9975a-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9975a-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9975a-128">OUTPUTS</span></span>

## <span data-ttu-id="9975a-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9975a-129">NOTES</span></span>

## <span data-ttu-id="9975a-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9975a-130">RELATED LINKS</span></span>

[<span data-ttu-id="9975a-131">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9975a-131">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="9975a-132">Yeni-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9975a-132">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="9975a-133">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9975a-133">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


