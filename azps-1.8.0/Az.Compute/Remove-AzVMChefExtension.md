---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 052082672dd822b78ff6c47abf7710c87c35a746
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917307"
---
# <span data-ttu-id="d56d0-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="d56d0-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="d56d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d56d0-102">SYNOPSIS</span></span>
<span data-ttu-id="d56d0-103">Sanal makineden Chef uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d56d0-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="d56d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d56d0-104">SYNTAX</span></span>

### <span data-ttu-id="d56d0-105">UX</span><span class="sxs-lookup"><span data-stu-id="d56d0-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d56d0-106">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="d56d0-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d56d0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d56d0-107">DESCRIPTION</span></span>
<span data-ttu-id="d56d0-108">**Remove-AzVMChefExtension** cmdlet 'i sanal makineden Chef uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d56d0-108">The **Remove-AzVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="d56d0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d56d0-109">EXAMPLES</span></span>

### <span data-ttu-id="d56d0-110">Örnek 1: Windows sanal makinesinden Chef uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d56d0-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="d56d0-111">Bu komut, ResourceGroup001 adındaki kaynak grubuna ait olan WindowsVM001 adındaki Windows tabanlı bir sanal makineden Chef uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d56d0-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="d56d0-112">Örnek 2: Linux sanal makinesinden Chef uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d56d0-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="d56d0-113">Bu komut, LinuxVM001 adındaki bir Linux tabanlı sanal makineden ResourceGroup002 adındaki kaynak grubuna ait bir Chef uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d56d0-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="d56d0-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d56d0-114">PARAMETERS</span></span>

### <span data-ttu-id="d56d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d56d0-115">-DefaultProfile</span></span>
<span data-ttu-id="d56d0-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d56d0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d56d0-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="d56d0-117">-Linux</span></span>
<span data-ttu-id="d56d0-118">Bu cmdlet 'in bir Linux sanal makinesini hedeflediği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="d56d0-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56d0-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d56d0-119">-Name</span></span>
<span data-ttu-id="d56d0-120">Bu cmdlet 'in kaldırıldığı Chef uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d56d0-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d56d0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d56d0-121">-ResourceGroupName</span></span>
<span data-ttu-id="d56d0-122">Sanal makineyi içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d56d0-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="d56d0-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="d56d0-123">-VMName</span></span>
<span data-ttu-id="d56d0-124">Bu cmdlet 'in Chef uzantısını kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d56d0-124">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="d56d0-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="d56d0-125">-Windows</span></span>
<span data-ttu-id="d56d0-126">Bu cmdlet 'in Windows sanal makinesini hedeflediği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="d56d0-126">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56d0-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="d56d0-127">-Confirm</span></span>
<span data-ttu-id="d56d0-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d56d0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d56d0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d56d0-129">-WhatIf</span></span>
<span data-ttu-id="d56d0-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d56d0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d56d0-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d56d0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d56d0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d56d0-132">CommonParameters</span></span>
<span data-ttu-id="d56d0-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d56d0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d56d0-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d56d0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d56d0-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d56d0-135">INPUTS</span></span>

### <span data-ttu-id="d56d0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d56d0-136">System.String</span></span>

## <span data-ttu-id="d56d0-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d56d0-137">OUTPUTS</span></span>

### <span data-ttu-id="d56d0-138">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d56d0-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d56d0-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d56d0-139">NOTES</span></span>

## <span data-ttu-id="d56d0-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d56d0-140">RELATED LINKS</span></span>

[<span data-ttu-id="d56d0-141">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="d56d0-141">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="d56d0-142">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="d56d0-142">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
