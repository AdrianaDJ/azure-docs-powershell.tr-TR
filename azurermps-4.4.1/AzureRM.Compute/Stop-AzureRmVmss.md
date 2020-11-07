---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 11b387e4022bce98e1275bb2af09bc97beff0041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763125"
---
# <span data-ttu-id="81078-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81078-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="81078-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81078-102">SYNOPSIS</span></span>
<span data-ttu-id="81078-103">VMSS 'yi veya VMSS içindeki sanal makinelerin kümesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="81078-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81078-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81078-104">SYNTAX</span></span>

### <span data-ttu-id="81078-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="81078-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81078-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="81078-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81078-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="81078-107">DESCRIPTION</span></span>
<span data-ttu-id="81078-108">**Stop-AzureRmVmss** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) veya sanal makine kümesi içindeki tüm sanal makineleri durdurur.</span><span class="sxs-lookup"><span data-stu-id="81078-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="81078-109">*InstanceId* parametresini kullanarak bir sanal makine kümesi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="81078-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="81078-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81078-110">EXAMPLES</span></span>

### <span data-ttu-id="81078-111">Örnek 1: VMSS içindeki tüm sanal makineleri durdurma</span><span class="sxs-lookup"><span data-stu-id="81078-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="81078-112">Bu komut, ContosoVMSS adlı VMSS 'ye ait tüm sanal makineleri durdurur.</span><span class="sxs-lookup"><span data-stu-id="81078-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="81078-113">Örnek 2: VMSS içinde belirli bir sanal makine kümesini durdurma</span><span class="sxs-lookup"><span data-stu-id="81078-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="81078-114">Bu komut, ContosoVMSS adlı VMSS 'ye ait örnek KIMLIĞI dizesi dizisiyle belirtilen belirli bir sanal makine kümesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="81078-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="81078-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81078-115">PARAMETERS</span></span>

### <span data-ttu-id="81078-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81078-116">-DefaultProfile</span></span>
<span data-ttu-id="81078-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="81078-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81078-118">-Force</span><span class="sxs-lookup"><span data-stu-id="81078-118">-Force</span></span>
<span data-ttu-id="81078-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="81078-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="81078-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="81078-120">-InstanceId</span></span>
<span data-ttu-id="81078-121">Bu cmdlet 'in durdurduğu sanal makine örneklerinin KIMLIĞINI veya kimliklerini dize dizisi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="81078-121">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="81078-122">Örneğin: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="81078-122">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81078-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81078-123">-ResourceGroupName</span></span>
<span data-ttu-id="81078-124">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81078-124">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81078-125">-Staysağlandı</span><span class="sxs-lookup"><span data-stu-id="81078-125">-StayProvisioned</span></span>
<span data-ttu-id="81078-126">Belirtilmişse, sanal makine durdurulmuş duruma girer.</span><span class="sxs-lookup"><span data-stu-id="81078-126">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="81078-127">Belirtilmezse, sanal makine durduruldu-serbest işlem durumuna girer.</span><span class="sxs-lookup"><span data-stu-id="81078-127">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="81078-128">Kullanıcı hala durdurulmuş durumda VM 'Ler için ücretlendirilecek, ancak durdurulan serbest durumda VM 'Ler için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="81078-128">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81078-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="81078-129">-VMScaleSetName</span></span>
<span data-ttu-id="81078-130">Bu cmdlet 'in sanal makineleri durdurduğu VMSS adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81078-130">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81078-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="81078-131">-Confirm</span></span>
<span data-ttu-id="81078-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="81078-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81078-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81078-133">-WhatIf</span></span>
<span data-ttu-id="81078-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="81078-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81078-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="81078-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81078-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81078-136">CommonParameters</span></span>
<span data-ttu-id="81078-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81078-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81078-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81078-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81078-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81078-139">INPUTS</span></span>

## <span data-ttu-id="81078-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81078-140">OUTPUTS</span></span>

## <span data-ttu-id="81078-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81078-141">NOTES</span></span>

## <span data-ttu-id="81078-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81078-142">RELATED LINKS</span></span>

[<span data-ttu-id="81078-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81078-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="81078-144">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81078-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="81078-145">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81078-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="81078-146">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81078-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="81078-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81078-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="81078-148">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81078-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="81078-149">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81078-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


