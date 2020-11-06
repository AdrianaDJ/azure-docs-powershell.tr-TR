---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: 44022fe8ea12c8f341952bd023aa41bf4ead92c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591786"
---
# <span data-ttu-id="5a5c4-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5a5c4-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="5a5c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a5c4-102">SYNOPSIS</span></span>
<span data-ttu-id="5a5c4-103">Bir VMSUBNET 'in durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5a5c4-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a5c4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a5c4-104">SYNTAX</span></span>

```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a5c4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a5c4-105">DESCRIPTION</span></span>
<span data-ttu-id="5a5c4-106">**Update-AzureRmVmss** cmdlet 'ı sanal makine ölçek kümesi 'nın (VMSS) durumunu yerel BIR VMSS nesnesinin durumuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5a5c4-106">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="5a5c4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a5c4-107">EXAMPLES</span></span>

### <span data-ttu-id="5a5c4-108">Örnek 1: bir VMSS durumunu yerel bir VMSS nesnesinin durumuna güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="5a5c4-108">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet "LocalVMSS"
```

<span data-ttu-id="5a5c4-109">Bu komut, Group001 adındaki kaynak grubuna ait olan ve VMSS001 adındaki kaynak grubuna ait olan, LocalVMSS adlı yerel bir VMSS nesnesinin durumuna ait durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5a5c4-109">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object named LocalVMSS.</span></span>

## <span data-ttu-id="5a5c4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a5c4-110">PARAMETERS</span></span>

### <span data-ttu-id="5a5c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a5c4-111">-DefaultProfile</span></span>
<span data-ttu-id="5a5c4-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5a5c4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a5c4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a5c4-113">-ResourceGroupName</span></span>
<span data-ttu-id="5a5c4-114">VMSS 'nin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a5c4-114">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="5a5c4-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5a5c4-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5a5c4-116">Yerel bir VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a5c4-116">Specifies a local VMSS object.</span></span>
<span data-ttu-id="5a5c4-117">Bir VMSS nesnesi edinmek için Get-AzureRmVmss cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5a5c4-117">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="5a5c4-118">Bu sanal makine nesnesi, VMSS 'nin güncelleştirilmiş durumunu içerir.</span><span class="sxs-lookup"><span data-stu-id="5a5c4-118">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a5c4-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5a5c4-119">-VMScaleSetName</span></span>
<span data-ttu-id="5a5c4-120">Bu cmdlet 'in oluşturduğu VMSS 'nin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a5c4-120">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5a5c4-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="5a5c4-121">-Confirm</span></span>
<span data-ttu-id="5a5c4-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5a5c4-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a5c4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a5c4-123">-WhatIf</span></span>
<span data-ttu-id="5a5c4-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5a5c4-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5a5c4-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5a5c4-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a5c4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a5c4-126">CommonParameters</span></span>
<span data-ttu-id="5a5c4-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a5c4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a5c4-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a5c4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a5c4-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a5c4-129">INPUTS</span></span>

## <span data-ttu-id="5a5c4-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a5c4-130">OUTPUTS</span></span>

## <span data-ttu-id="5a5c4-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a5c4-131">NOTES</span></span>

## <span data-ttu-id="5a5c4-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a5c4-132">RELATED LINKS</span></span>

[<span data-ttu-id="5a5c4-133">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5a5c4-133">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="5a5c4-134">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5a5c4-134">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="5a5c4-135">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5a5c4-135">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="5a5c4-136">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5a5c4-136">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="5a5c4-137">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5a5c4-137">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="5a5c4-138">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5a5c4-138">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="5a5c4-139">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5a5c4-139">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


