---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssRollingUpgradePolicy.md
ms.openlocfilehash: dc147fa18d4db87b9a72aaf497f9fac59ea2a864
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586916"
---
# <span data-ttu-id="b5a0f-101">Set-AzureRmVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="b5a0f-101">Set-AzureRmVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="b5a0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5a0f-102">SYNOPSIS</span></span>
<span data-ttu-id="b5a0f-103">VMSS çalışırken yükseltme ilkesi özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b5a0f-103">Sets the VMSS rolling upgrade policy properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5a0f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5a0f-104">SYNTAX</span></span>

```
Set-AzureRmVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5a0f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5a0f-105">DESCRIPTION</span></span>
<span data-ttu-id="b5a0f-106">VMSS çalışırken yükseltme ilkesi özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b5a0f-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="b5a0f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5a0f-107">EXAMPLES</span></span>

### <span data-ttu-id="b5a0f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b5a0f-108">Example 1</span></span>
```
PS C:\> Set-AzureRmVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="b5a0f-109">Bu komut Maxbatchınstance için yüzde 40, Maxunhealthyınstance için yüzde 35, maxunhealthyyükselt$vmss Endeğeri</span><span class="sxs-lookup"><span data-stu-id="b5a0f-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="b5a0f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5a0f-110">PARAMETERS</span></span>

### <span data-ttu-id="b5a0f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5a0f-111">-DefaultProfile</span></span>
<span data-ttu-id="b5a0f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5a0f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5a0f-113">-Maxbatchınstancepercent</span><span class="sxs-lookup"><span data-stu-id="b5a0f-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="b5a0f-114">Tek bir toplu işlemde çalışırken yükseltme tarafından aynı anda Yükseltilecek toplam sanal makine örneklerinin en yüksek yüzdesi.</span><span class="sxs-lookup"><span data-stu-id="b5a0f-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="b5a0f-115">Bu en yüksek düzeyde, önceki veya gelecekteki toplu işlemdeki sağlıksız örnekler, daha yüksek güvenilirlik sağlamak amacıyla toplu işteki örneklerin yüzdesine neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="b5a0f-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="b5a0f-116">Değer belirtilmezse, 20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="b5a0f-116">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a0f-117">-Maxunhealthyınstancepercent</span><span class="sxs-lookup"><span data-stu-id="b5a0f-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="b5a0f-118">Ölçek kümesindeki toplam sanal makine örneklerinin, yükseltilme sonucu olarak, yükseltme sonucu olan veya çalışırken yükseltme iptal edilmeden önce sanal makine durumu denetimleri tarafından sağlıksız bir durumda bulunabildiği en yüksek oranı.</span><span class="sxs-lookup"><span data-stu-id="b5a0f-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="b5a0f-119">Bu kısıtlama, toplu işlem başlatılmadan önce işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="b5a0f-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="b5a0f-120">Değer belirtilmezse, 20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="b5a0f-120">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a0f-121">-Maxunhealthyyükseltildi Dedınstancepercent</span><span class="sxs-lookup"><span data-stu-id="b5a0f-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="b5a0f-122">Sağlıksız durumda olabilecek en yüksek yükseltilmiş sanal makine örneği yüzdesi.</span><span class="sxs-lookup"><span data-stu-id="b5a0f-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="b5a0f-123">Bu denetim her toplu iş yükseltildikten sonra gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="b5a0f-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="b5a0f-124">Bu yüzde aşılırsa, çalışırken güncelleştirme iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="b5a0f-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="b5a0f-125">Değer belirtilmezse, 20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="b5a0f-125">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a0f-126">-Pausetimebetweentoplu Işler</span><span class="sxs-lookup"><span data-stu-id="b5a0f-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="b5a0f-127">Bir toplu işteki tüm sanal makinelerin güncelleştirmesini tamamlama ve sonraki toplu işlemi başlatma arasındaki bekleme süresi.</span><span class="sxs-lookup"><span data-stu-id="b5a0f-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="b5a0f-128">Süre ISO 8601 biçiminde belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="b5a0f-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="b5a0f-129">Varsayılan değer 0 saniyedir (PT0S).</span><span class="sxs-lookup"><span data-stu-id="b5a0f-129">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a0f-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b5a0f-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b5a0f-131">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5a0f-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="b5a0f-132">Nesneyi oluşturmak için New-AzureRmVmssConfig cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5a0f-132">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a0f-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="b5a0f-133">-Confirm</span></span>
<span data-ttu-id="b5a0f-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b5a0f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5a0f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5a0f-135">-WhatIf</span></span>
<span data-ttu-id="b5a0f-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5a0f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5a0f-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b5a0f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5a0f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5a0f-138">CommonParameters</span></span>
<span data-ttu-id="b5a0f-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5a0f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5a0f-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5a0f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5a0f-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5a0f-141">INPUTS</span></span>

### <span data-ttu-id="b5a0f-142">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b5a0f-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>
<span data-ttu-id="b5a0f-143">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String</span><span class="sxs-lookup"><span data-stu-id="b5a0f-143">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="b5a0f-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5a0f-144">OUTPUTS</span></span>

### <span data-ttu-id="b5a0f-145">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b5a0f-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b5a0f-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5a0f-146">NOTES</span></span>

## <span data-ttu-id="b5a0f-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5a0f-147">RELATED LINKS</span></span>

