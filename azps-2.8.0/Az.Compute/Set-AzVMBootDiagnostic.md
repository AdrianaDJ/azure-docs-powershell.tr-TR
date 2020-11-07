---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
ms.openlocfilehash: 7ec034ed0d84b0c45486d17adbdb5c0a152d27b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752698"
---
# <span data-ttu-id="3d603-101">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3d603-101">Set-AzVMBootDiagnostic</span></span>

## <span data-ttu-id="3d603-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d603-102">SYNOPSIS</span></span>
<span data-ttu-id="3d603-103">Sanal makinenin önyükleme tanılaması özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3d603-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="3d603-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d603-104">SYNTAX</span></span>

### <span data-ttu-id="3d603-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="3d603-105">EnableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d603-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="3d603-106">DisableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d603-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d603-107">DESCRIPTION</span></span>
<span data-ttu-id="3d603-108">**Set-AzVMBootDiagnostic** cmdlet 'i sanal makinenin önyükleme tanılaması özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3d603-108">The **Set-AzVMBootDiagnostic** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="3d603-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d603-109">EXAMPLES</span></span>

### <span data-ttu-id="3d603-110">Örnek 1: önyükleme tanılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="3d603-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzVMBootDiagnostic -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="3d603-111">İlk komut ContosoVM07 adındaki sanal makineyi **Get-AzVM** kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="3d603-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="3d603-112">Komut, $VM değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3d603-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="3d603-113">İkinci komut $VM sanal makinesi için önyükleme tanılaması 'nı mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="3d603-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="3d603-114">Tanılama verileri belirtilen hesapta depolanır.</span><span class="sxs-lookup"><span data-stu-id="3d603-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="3d603-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d603-115">PARAMETERS</span></span>

### <span data-ttu-id="3d603-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d603-116">-DefaultProfile</span></span>
<span data-ttu-id="3d603-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3d603-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d603-118">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="3d603-118">-Disable</span></span>
<span data-ttu-id="3d603-119">Bu cmdlet 'in sanal makinenin önyükleme tanılamasını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d603-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d603-120">-Enable</span><span class="sxs-lookup"><span data-stu-id="3d603-120">-Enable</span></span>
<span data-ttu-id="3d603-121">Bu cmdlet 'in sanal makine için önyükleme tanılamayı etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d603-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d603-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d603-122">-ResourceGroupName</span></span>
<span data-ttu-id="3d603-123">Depolama hesabı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d603-123">Specifies the name of the resource group of storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d603-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3d603-124">-StorageAccountName</span></span>
<span data-ttu-id="3d603-125">Önyükleme tanılaması verilerinin kaydedileceği depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d603-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d603-126">-VM</span><span class="sxs-lookup"><span data-stu-id="3d603-126">-VM</span></span>
<span data-ttu-id="3d603-127">Bu cmdlet 'in önyükleme tanılamasını değiştirdiği sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d603-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="3d603-128">Sanal makine nesnesi edinmek için Get-AzVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3d603-128">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d603-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d603-129">CommonParameters</span></span>
<span data-ttu-id="3d603-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d603-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d603-131">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3d603-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d603-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d603-132">INPUTS</span></span>

### <span data-ttu-id="3d603-133">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3d603-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="3d603-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3d603-134">System.String</span></span>

## <span data-ttu-id="3d603-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d603-135">OUTPUTS</span></span>

### <span data-ttu-id="3d603-136">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3d603-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="3d603-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d603-137">NOTES</span></span>

## <span data-ttu-id="3d603-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d603-138">RELATED LINKS</span></span>

[<span data-ttu-id="3d603-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="3d603-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="3d603-140">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="3d603-140">Get-AzVMBootDiagnosticsData</span></span>](./Get-AzVMBootDiagnosticsData.md)


