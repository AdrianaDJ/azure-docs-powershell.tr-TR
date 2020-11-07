---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVmss.md
ms.openlocfilehash: b0e01f462bfb7576e942138cb42b3171fb6660b3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936884"
---
# <span data-ttu-id="27b12-101">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27b12-101">Restart-AzVmss</span></span>

## <span data-ttu-id="27b12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27b12-102">SYNOPSIS</span></span>
<span data-ttu-id="27b12-103">Vmsubnet 'de VMSS veya sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="27b12-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

## <span data-ttu-id="27b12-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27b12-104">SYNTAX</span></span>

```
Restart-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27b12-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="27b12-105">DESCRIPTION</span></span>
<span data-ttu-id="27b12-106">**Restart-AzVmss** cmdlet 'ı sanal makine ölçeği kümesini (VMSS) yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="27b12-106">The **Restart-AzVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="27b12-107">Bu cmdlet, *InstanceId* parametresini kullanarak VMSS içinde belirli bir sanal makineyi yeniden başlatmak için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="27b12-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="27b12-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27b12-108">EXAMPLES</span></span>

### <span data-ttu-id="27b12-109">Örnek 1: VMSS 'yi yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="27b12-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="27b12-110">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS 'yi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="27b12-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="27b12-111">Örnek 2: VMSS içinde belirli bir sanal makineyi yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="27b12-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="27b12-112">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS 'de 1 örnek KIMLIĞINE sahip bir sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="27b12-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="27b12-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27b12-113">PARAMETERS</span></span>

### <span data-ttu-id="27b12-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="27b12-114">-AsJob</span></span>
<span data-ttu-id="27b12-115">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="27b12-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="27b12-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27b12-116">-DefaultProfile</span></span>
<span data-ttu-id="27b12-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="27b12-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27b12-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="27b12-118">-InstanceId</span></span>
<span data-ttu-id="27b12-119">Dize dizisi olarak, yeniden başlatılması gereken örneklerin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="27b12-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="27b12-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27b12-120">-ResourceGroupName</span></span>
<span data-ttu-id="27b12-121">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27b12-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="27b12-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="27b12-122">-VMScaleSetName</span></span>
<span data-ttu-id="27b12-123">Türleri, bu cmdlet 'in yeniden başlattığı VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="27b12-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="27b12-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="27b12-124">-Confirm</span></span>
<span data-ttu-id="27b12-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="27b12-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27b12-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27b12-126">-WhatIf</span></span>
<span data-ttu-id="27b12-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="27b12-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27b12-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="27b12-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27b12-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27b12-129">CommonParameters</span></span>
<span data-ttu-id="27b12-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27b12-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27b12-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27b12-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27b12-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27b12-132">INPUTS</span></span>

### <span data-ttu-id="27b12-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="27b12-133">None</span></span>
<span data-ttu-id="27b12-134">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="27b12-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="27b12-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27b12-135">OUTPUTS</span></span>

###  
<span data-ttu-id="27b12-136">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="27b12-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="27b12-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27b12-137">NOTES</span></span>

## <span data-ttu-id="27b12-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27b12-138">RELATED LINKS</span></span>

[<span data-ttu-id="27b12-139">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27b12-139">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="27b12-140">Yeni-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27b12-140">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="27b12-141">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27b12-141">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="27b12-142">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27b12-142">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="27b12-143">Başlangıç-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27b12-143">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="27b12-144">Dur-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27b12-144">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="27b12-145">Güncelleştirme-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27b12-145">Update-AzVmss</span></span>](./Update-AzVmss.md)


