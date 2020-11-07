---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: edf0ab0784288f6a700dc82a77a66846a5806826
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761352"
---
# <span data-ttu-id="aa51d-101">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="aa51d-101">Get-AzVMAccessExtension</span></span>

## <span data-ttu-id="aa51d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa51d-102">SYNOPSIS</span></span>
<span data-ttu-id="aa51d-103">VMAccess uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="aa51d-103">Gets information about the VMAccess extension.</span></span>

## <span data-ttu-id="aa51d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aa51d-104">SYNTAX</span></span>

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa51d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aa51d-105">DESCRIPTION</span></span>
<span data-ttu-id="aa51d-106">**Get-Azvmaccessextenma** cmdlet 'ı sanal makine erişimi (VMAccess) sanal makine uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="aa51d-106">The **Get-AzVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="aa51d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aa51d-107">EXAMPLES</span></span>

### <span data-ttu-id="aa51d-108">Örnek 1: VMAccess uzantısını alma</span><span class="sxs-lookup"><span data-stu-id="aa51d-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="aa51d-109">Bu komut, VirtualMachine07 adındaki sanal makine için ContosoTest adındaki VMAccess uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="aa51d-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="aa51d-110">Örnek 2: VMAccess uzantısının örnek görünümünü alma</span><span class="sxs-lookup"><span data-stu-id="aa51d-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="aa51d-111">Bu komut, VirtualMachine07 adındaki sanal makine için ContosoTest adındaki VMAccess uzantısının örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="aa51d-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="aa51d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aa51d-112">PARAMETERS</span></span>

### <span data-ttu-id="aa51d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa51d-113">-DefaultProfile</span></span>
<span data-ttu-id="aa51d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aa51d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa51d-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="aa51d-115">-Name</span></span>
<span data-ttu-id="aa51d-116">Bu cmdlet 'in aldığı uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa51d-116">Specifies the name of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa51d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa51d-117">-ResourceGroupName</span></span>
<span data-ttu-id="aa51d-118">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa51d-118">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa51d-119">-Durum</span><span class="sxs-lookup"><span data-stu-id="aa51d-119">-Status</span></span>
<span data-ttu-id="aa51d-120">Bu cmdlet 'in yalnızca uzantının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aa51d-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa51d-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="aa51d-121">-VMName</span></span>
<span data-ttu-id="aa51d-122">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa51d-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="aa51d-123">Bu cmdlet, bu parametrenin belirttiği sanal makinede VMAccess hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="aa51d-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa51d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa51d-124">CommonParameters</span></span>
<span data-ttu-id="aa51d-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aa51d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa51d-126">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="aa51d-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa51d-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aa51d-127">INPUTS</span></span>

### <span data-ttu-id="aa51d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="aa51d-128">System.String</span></span>

### <span data-ttu-id="aa51d-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="aa51d-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="aa51d-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aa51d-130">OUTPUTS</span></span>

### <span data-ttu-id="aa51d-131">Microsoft. Azure. Commands. COMPUTE. modeller. VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="aa51d-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="aa51d-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aa51d-132">NOTES</span></span>

## <span data-ttu-id="aa51d-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aa51d-133">RELATED LINKS</span></span>

[<span data-ttu-id="aa51d-134">Remove-azvmaccessexten</span><span class="sxs-lookup"><span data-stu-id="aa51d-134">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="aa51d-135">Set-azvmaccessexten</span><span class="sxs-lookup"><span data-stu-id="aa51d-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="aa51d-136">Get-Azvmexgeri</span><span class="sxs-lookup"><span data-stu-id="aa51d-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)


