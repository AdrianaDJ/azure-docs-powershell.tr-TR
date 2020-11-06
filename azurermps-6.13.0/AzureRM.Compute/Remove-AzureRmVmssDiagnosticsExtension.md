---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 52b090f433d3d605c870025d696b2572e6938330
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593293"
---
# <span data-ttu-id="307aa-101">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="307aa-101">Remove-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="307aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="307aa-102">SYNOPSIS</span></span>
<span data-ttu-id="307aa-103">Bir tanılama uzantısını VMSS 'den kaldırır.</span><span class="sxs-lookup"><span data-stu-id="307aa-103">Removes a diagnostics extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="307aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="307aa-104">SYNTAX</span></span>

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="307aa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="307aa-105">DESCRIPTION</span></span>
<span data-ttu-id="307aa-106">**Remove-Azurermvmssdiagnosticsextencmdlet** 'ı sanal makine ölçek kümesinden (VMSS) bir tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="307aa-106">The **Remove-AzureRmVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="307aa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="307aa-107">EXAMPLES</span></span>

### <span data-ttu-id="307aa-108">Örnek 1: VMSS 'den tanılama uzantısı kaldırma</span><span class="sxs-lookup"><span data-stu-id="307aa-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="307aa-109">Bu komut, VMSS 'den tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="307aa-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="307aa-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="307aa-110">PARAMETERS</span></span>

### <span data-ttu-id="307aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="307aa-111">-DefaultProfile</span></span>
<span data-ttu-id="307aa-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="307aa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="307aa-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="307aa-113">-Name</span></span>
<span data-ttu-id="307aa-114">Bu cmdlet 'in kaldırıldığı uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="307aa-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="307aa-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="307aa-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="307aa-116">Uzantının kaldırılacağı VMSS 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="307aa-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="307aa-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="307aa-117">-Confirm</span></span>
<span data-ttu-id="307aa-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="307aa-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="307aa-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="307aa-119">-WhatIf</span></span>
<span data-ttu-id="307aa-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="307aa-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="307aa-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="307aa-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="307aa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="307aa-122">CommonParameters</span></span>
<span data-ttu-id="307aa-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="307aa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="307aa-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="307aa-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="307aa-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="307aa-125">INPUTS</span></span>

### <span data-ttu-id="307aa-126">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="307aa-126">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

### <span data-ttu-id="307aa-127">System. String</span><span class="sxs-lookup"><span data-stu-id="307aa-127">System.String</span></span>

## <span data-ttu-id="307aa-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="307aa-128">OUTPUTS</span></span>

### <span data-ttu-id="307aa-129">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="307aa-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="307aa-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="307aa-130">NOTES</span></span>

## <span data-ttu-id="307aa-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="307aa-131">RELATED LINKS</span></span>

[<span data-ttu-id="307aa-132">Add-azurermvmssdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="307aa-132">Add-AzureRmVmssDiagnosticsExtension</span></span>](./Add-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="307aa-133">Remove-azurermvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="307aa-133">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="307aa-134">Remove-Azurermvmssextenma</span><span class="sxs-lookup"><span data-stu-id="307aa-134">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)


