---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 6582b8d0a141522e6ac8bb4dad23f1da5e31000d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939946"
---
# <span data-ttu-id="0f3ea-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0f3ea-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="0f3ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f3ea-102">SYNOPSIS</span></span>
<span data-ttu-id="0f3ea-103">Vmsubnet 'de VMSS veya sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f3ea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f3ea-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f3ea-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f3ea-105">DESCRIPTION</span></span>
<span data-ttu-id="0f3ea-106">**Restart-AzureRmVmss** cmdlet 'ı sanal makine ölçek kümesini (VMSS) yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="0f3ea-107">Bu cmdlet, *InstanceId* parametresini kullanarak VMSS içinde belirli bir sanal makineyi yeniden başlatmak için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="0f3ea-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f3ea-108">EXAMPLES</span></span>

### <span data-ttu-id="0f3ea-109">Örnek 1: VMSS 'yi yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="0f3ea-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="0f3ea-110">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS 'yi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="0f3ea-111">Örnek 2: VMSS içinde belirli bir sanal makineyi yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="0f3ea-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="0f3ea-112">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS 'de 1 örnek KIMLIĞINE sahip bir sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="0f3ea-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f3ea-113">PARAMETERS</span></span>

### <span data-ttu-id="0f3ea-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="0f3ea-114">-AsJob</span></span>
<span data-ttu-id="0f3ea-115">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0f3ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f3ea-116">-DefaultProfile</span></span>
<span data-ttu-id="0f3ea-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f3ea-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="0f3ea-118">-InstanceId</span></span>
<span data-ttu-id="0f3ea-119">Dize dizisi olarak, yeniden başlatılması gereken örneklerin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="0f3ea-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f3ea-120">-ResourceGroupName</span></span>
<span data-ttu-id="0f3ea-121">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="0f3ea-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0f3ea-122">-VMScaleSetName</span></span>
<span data-ttu-id="0f3ea-123">Türleri, bu cmdlet 'in yeniden başlattığı VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="0f3ea-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="0f3ea-124">-Confirm</span></span>
<span data-ttu-id="0f3ea-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f3ea-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f3ea-126">-WhatIf</span></span>
<span data-ttu-id="0f3ea-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f3ea-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f3ea-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f3ea-129">CommonParameters</span></span>
<span data-ttu-id="0f3ea-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f3ea-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f3ea-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f3ea-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f3ea-132">INPUTS</span></span>

### <span data-ttu-id="0f3ea-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0f3ea-133">None</span></span>
<span data-ttu-id="0f3ea-134">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0f3ea-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f3ea-135">OUTPUTS</span></span>

###  
<span data-ttu-id="0f3ea-136">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="0f3ea-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f3ea-137">NOTES</span></span>

## <span data-ttu-id="0f3ea-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f3ea-138">RELATED LINKS</span></span>

[<span data-ttu-id="0f3ea-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0f3ea-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="0f3ea-140">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0f3ea-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="0f3ea-141">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0f3ea-141">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="0f3ea-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0f3ea-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="0f3ea-143">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0f3ea-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="0f3ea-144">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0f3ea-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="0f3ea-145">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0f3ea-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


