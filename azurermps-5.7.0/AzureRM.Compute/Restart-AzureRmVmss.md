---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
ms.openlocfilehash: 1bc6b2b3ceb7ed7f991c92e4b8f8b034c78d54d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594120"
---
# <span data-ttu-id="96e97-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="96e97-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="96e97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96e97-102">SYNOPSIS</span></span>
<span data-ttu-id="96e97-103">Vmsubnet 'de VMSS veya sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="96e97-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96e97-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="96e97-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96e97-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="96e97-105">DESCRIPTION</span></span>
<span data-ttu-id="96e97-106">**Restart-AzureRmVmss** cmdlet 'ı sanal makine ölçek kümesini (VMSS) yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="96e97-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="96e97-107">Bu cmdlet, *InstanceId* parametresini kullanarak VMSS içinde belirli bir sanal makineyi yeniden başlatmak için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="96e97-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="96e97-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="96e97-108">EXAMPLES</span></span>

### <span data-ttu-id="96e97-109">Örnek 1: VMSS 'yi yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="96e97-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="96e97-110">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS 'yi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="96e97-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="96e97-111">Örnek 2: VMSS içinde belirli bir sanal makineyi yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="96e97-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="96e97-112">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS 'de 1 örnek KIMLIĞINE sahip bir sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="96e97-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="96e97-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="96e97-113">PARAMETERS</span></span>

### <span data-ttu-id="96e97-114">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="96e97-114">-InstanceId</span></span>
<span data-ttu-id="96e97-115">Dize dizisi olarak, yeniden başlatılması gereken örneklerin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="96e97-115">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96e97-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96e97-116">-ResourceGroupName</span></span>
<span data-ttu-id="96e97-117">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="96e97-117">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="96e97-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="96e97-118">-VMScaleSetName</span></span>
<span data-ttu-id="96e97-119">Türleri, bu cmdlet 'in yeniden başlattığı VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="96e97-119">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="96e97-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="96e97-120">-Confirm</span></span>
<span data-ttu-id="96e97-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="96e97-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96e97-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96e97-122">-WhatIf</span></span>
<span data-ttu-id="96e97-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="96e97-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96e97-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="96e97-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96e97-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96e97-125">CommonParameters</span></span>
<span data-ttu-id="96e97-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="96e97-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96e97-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96e97-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96e97-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="96e97-128">INPUTS</span></span>

### <span data-ttu-id="96e97-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="96e97-129">None</span></span>
<span data-ttu-id="96e97-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="96e97-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="96e97-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="96e97-131">OUTPUTS</span></span>

###  
<span data-ttu-id="96e97-132">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="96e97-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="96e97-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="96e97-133">NOTES</span></span>

## <span data-ttu-id="96e97-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="96e97-134">RELATED LINKS</span></span>

[<span data-ttu-id="96e97-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="96e97-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="96e97-136">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="96e97-136">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="96e97-137">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="96e97-137">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="96e97-138">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="96e97-138">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="96e97-139">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="96e97-139">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="96e97-140">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="96e97-140">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="96e97-141">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="96e97-141">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


