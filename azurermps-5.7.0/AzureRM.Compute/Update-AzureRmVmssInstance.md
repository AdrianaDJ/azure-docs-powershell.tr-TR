---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
ms.openlocfilehash: 75b8190c34d5335904d40d386cabc76e8cbf0b0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586758"
---
# <span data-ttu-id="68331-101">Update-AzureRmVmssInstance</span><span class="sxs-lookup"><span data-stu-id="68331-101">Update-AzureRmVmssInstance</span></span>

## <span data-ttu-id="68331-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68331-102">SYNOPSIS</span></span>
<span data-ttu-id="68331-103">VMSS örneğinin el ile yükseltilmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="68331-103">Starts a manual upgrade of the VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68331-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68331-104">SYNTAX</span></span>

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68331-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="68331-105">DESCRIPTION</span></span>
<span data-ttu-id="68331-106">Update-AzureRmVmssInstance cmdlet 'i, belirtilen sanal makine ölçek kümesi (VMSS) örneğinin el ile yükseltilmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="68331-106">The Update-AzureRmVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="68331-107">Bu, VMSS ölçek kümesindeki yükseltme ilkesi el ile olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="68331-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="68331-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68331-108">EXAMPLES</span></span>

### <span data-ttu-id="68331-109">Örnek 1: VMSS örneğinin yükseltmesini başlatma</span><span class="sxs-lookup"><span data-stu-id="68331-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="68331-110">Bu komut, VMScaleSet001 adında, örnek KIMLIĞI 0 olan bir yükseltme başlatır.</span><span class="sxs-lookup"><span data-stu-id="68331-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="68331-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68331-111">PARAMETERS</span></span>

### <span data-ttu-id="68331-112">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="68331-112">-InstanceId</span></span>
<span data-ttu-id="68331-113">Bir dize dizisi, Yükseltilecek olan Örneğin KIMLIĞINI veya kimliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="68331-113">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68331-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68331-114">-ResourceGroupName</span></span>
<span data-ttu-id="68331-115">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="68331-115">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="68331-116">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="68331-116">-VMScaleSetName</span></span>
<span data-ttu-id="68331-117">Bu cmdlet 'in yükseltmelerine sahip VMSS örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="68331-117">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68331-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="68331-118">-Confirm</span></span>
<span data-ttu-id="68331-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="68331-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68331-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68331-120">-WhatIf</span></span>
<span data-ttu-id="68331-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="68331-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="68331-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="68331-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68331-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68331-123">CommonParameters</span></span>
<span data-ttu-id="68331-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68331-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68331-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68331-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68331-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68331-126">INPUTS</span></span>

### <span data-ttu-id="68331-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="68331-127">None</span></span>
<span data-ttu-id="68331-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="68331-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="68331-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68331-129">OUTPUTS</span></span>

###  
<span data-ttu-id="68331-130">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="68331-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="68331-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68331-131">NOTES</span></span>

## <span data-ttu-id="68331-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68331-132">RELATED LINKS</span></span>

[<span data-ttu-id="68331-133">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="68331-133">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


