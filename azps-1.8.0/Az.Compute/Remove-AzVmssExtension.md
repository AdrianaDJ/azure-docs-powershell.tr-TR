---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: aeb07f9d9e2faaaf9fc09867fcfee045a5bc8351
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761269"
---
# <span data-ttu-id="dca93-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="dca93-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="dca93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dca93-102">SYNOPSIS</span></span>
<span data-ttu-id="dca93-103">Bir uzantıyı VMSS 'den kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dca93-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="dca93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dca93-104">SYNTAX</span></span>

### <span data-ttu-id="dca93-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dca93-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dca93-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="dca93-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dca93-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dca93-107">DESCRIPTION</span></span>
<span data-ttu-id="dca93-108">**Remove-AzVmssExtension** cmdlet 'ı sanal makine ölçek kümesinden (VMSS) uzantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dca93-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="dca93-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dca93-109">EXAMPLES</span></span>

### <span data-ttu-id="dca93-110">Örnek 1: VMSS uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="dca93-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="dca93-111">Bu komut bir VMSS uzantısını kaldırır ve değişiklikten sonra VMSS 'yi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dca93-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="dca93-112">Örnek 2: VMSUBNET 'den bir örneği kaldırma</span><span class="sxs-lookup"><span data-stu-id="dca93-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="dca93-113">Bu komut, Group002 adlı kaynak grubuna ait olan VMSS 'den bir uzantı kimliği belirtmeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dca93-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="dca93-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dca93-114">PARAMETERS</span></span>

### <span data-ttu-id="dca93-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dca93-115">-DefaultProfile</span></span>
<span data-ttu-id="dca93-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dca93-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca93-117">-ID</span><span class="sxs-lookup"><span data-stu-id="dca93-117">-Id</span></span>
<span data-ttu-id="dca93-118">Bu cmdlet 'in VMSUBNET 'den kaldırdığı uzantının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="dca93-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dca93-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="dca93-119">-Name</span></span>
<span data-ttu-id="dca93-120">Bu cmdlet 'in kaldırıldığı uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dca93-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dca93-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="dca93-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="dca93-122">Uzantısının kaldırılacağı VMSS 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="dca93-122">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="dca93-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="dca93-123">-Confirm</span></span>
<span data-ttu-id="dca93-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dca93-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dca93-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dca93-125">-WhatIf</span></span>
<span data-ttu-id="dca93-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dca93-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dca93-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dca93-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dca93-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca93-128">CommonParameters</span></span>
<span data-ttu-id="dca93-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dca93-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca93-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dca93-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca93-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dca93-131">INPUTS</span></span>

### <span data-ttu-id="dca93-132">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="dca93-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="dca93-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dca93-133">System.String</span></span>

## <span data-ttu-id="dca93-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dca93-134">OUTPUTS</span></span>

### <span data-ttu-id="dca93-135">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="dca93-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="dca93-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dca93-136">NOTES</span></span>

## <span data-ttu-id="dca93-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dca93-137">RELATED LINKS</span></span>

[<span data-ttu-id="dca93-138">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="dca93-138">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
