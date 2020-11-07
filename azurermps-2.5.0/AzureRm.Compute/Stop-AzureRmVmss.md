---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 50fd6447448968527b942e163f520142f594b7a6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939153"
---
# <span data-ttu-id="9c94e-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9c94e-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="9c94e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c94e-102">SYNOPSIS</span></span>
<span data-ttu-id="9c94e-103">VMSS 'yi veya VMSS içindeki sanal makinelerin kümesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="9c94e-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c94e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c94e-104">SYNTAX</span></span>

### <span data-ttu-id="9c94e-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9c94e-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c94e-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="9c94e-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c94e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c94e-107">DESCRIPTION</span></span>
<span data-ttu-id="9c94e-108">**Stop-AzureRmVmss** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) veya sanal makine kümesi içindeki tüm sanal makineleri durdurur.</span><span class="sxs-lookup"><span data-stu-id="9c94e-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="9c94e-109">*InstanceId* parametresini kullanarak bir sanal makine kümesi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c94e-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="9c94e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c94e-110">EXAMPLES</span></span>

### <span data-ttu-id="9c94e-111">Örnek 1: VMSS içindeki tüm sanal makineleri durdurma</span><span class="sxs-lookup"><span data-stu-id="9c94e-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="9c94e-112">Bu komut, ContosoVMSS adlı VMSS 'ye ait tüm sanal makineleri durdurur.</span><span class="sxs-lookup"><span data-stu-id="9c94e-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="9c94e-113">Örnek 2: VMSS içinde belirli bir sanal makine kümesini durdurma</span><span class="sxs-lookup"><span data-stu-id="9c94e-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="9c94e-114">Bu komut, ContosoVMSS adlı VMSS 'ye ait örnek KIMLIĞI dizesi dizisiyle belirtilen belirli bir sanal makine kümesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="9c94e-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="9c94e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c94e-115">PARAMETERS</span></span>

### <span data-ttu-id="9c94e-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="9c94e-116">-AsJob</span></span>
<span data-ttu-id="9c94e-117">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="9c94e-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9c94e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c94e-118">-DefaultProfile</span></span>
<span data-ttu-id="9c94e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9c94e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c94e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9c94e-120">-Force</span></span>
<span data-ttu-id="9c94e-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="9c94e-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9c94e-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="9c94e-122">-InstanceId</span></span>
<span data-ttu-id="9c94e-123">Bu cmdlet 'in durdurduğu sanal makine örneklerinin KIMLIĞINI veya kimliklerini dize dizisi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c94e-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="9c94e-124">Örneğin: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="9c94e-124">For instance: `-InstanceId "0", "3"`.</span></span>

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

### <span data-ttu-id="9c94e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c94e-125">-ResourceGroupName</span></span>
<span data-ttu-id="9c94e-126">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c94e-126">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="9c94e-127">-Staysağlandı</span><span class="sxs-lookup"><span data-stu-id="9c94e-127">-StayProvisioned</span></span>
<span data-ttu-id="9c94e-128">Belirtilmişse, sanal makine durdurulmuş duruma girer.</span><span class="sxs-lookup"><span data-stu-id="9c94e-128">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="9c94e-129">Belirtilmezse, sanal makine durduruldu-serbest işlem durumuna girer.</span><span class="sxs-lookup"><span data-stu-id="9c94e-129">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="9c94e-130">Kullanıcı hala durdurulmuş durumda VM 'Ler için ücretlendirilecek, ancak durdurulan serbest durumda VM 'Ler için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="9c94e-130">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c94e-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9c94e-131">-VMScaleSetName</span></span>
<span data-ttu-id="9c94e-132">Bu cmdlet 'in sanal makineleri durdurduğu VMSS adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c94e-132">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="9c94e-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="9c94e-133">-Confirm</span></span>
<span data-ttu-id="9c94e-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9c94e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c94e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c94e-135">-WhatIf</span></span>
<span data-ttu-id="9c94e-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9c94e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c94e-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9c94e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c94e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c94e-138">CommonParameters</span></span>
<span data-ttu-id="9c94e-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c94e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c94e-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c94e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c94e-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c94e-141">INPUTS</span></span>

### <span data-ttu-id="9c94e-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9c94e-142">None</span></span>
<span data-ttu-id="9c94e-143">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="9c94e-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9c94e-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c94e-144">OUTPUTS</span></span>

### <span data-ttu-id="9c94e-145">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="9c94e-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="9c94e-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c94e-146">NOTES</span></span>

## <span data-ttu-id="9c94e-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c94e-147">RELATED LINKS</span></span>

[<span data-ttu-id="9c94e-148">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9c94e-148">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="9c94e-149">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9c94e-149">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="9c94e-150">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9c94e-150">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="9c94e-151">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9c94e-151">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="9c94e-152">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9c94e-152">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="9c94e-153">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9c94e-153">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="9c94e-154">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9c94e-154">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


