---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
ms.openlocfilehash: dc2e22acf8efd18a565c1ede7ff22aeb21679a47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589859"
---
# <span data-ttu-id="18ffc-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="18ffc-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="18ffc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="18ffc-103">Sanal makineden Chef uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="18ffc-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18ffc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18ffc-104">SYNTAX</span></span>

### <span data-ttu-id="18ffc-105">UX</span><span class="sxs-lookup"><span data-stu-id="18ffc-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18ffc-106">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="18ffc-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18ffc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="18ffc-107">DESCRIPTION</span></span>
<span data-ttu-id="18ffc-108">**Remove-AzureVMChefExtension** cmdlet 'i sanal makineden Chef uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="18ffc-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="18ffc-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18ffc-109">EXAMPLES</span></span>

### <span data-ttu-id="18ffc-110">Örnek 1: Windows sanal makinesinden Chef uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="18ffc-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="18ffc-111">Bu komut, ResourceGroup001 adındaki kaynak grubuna ait olan WindowsVM001 adındaki Windows tabanlı bir sanal makineden Chef uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="18ffc-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="18ffc-112">Örnek 2: Linux sanal makinesinden Chef uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="18ffc-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="18ffc-113">Bu komut, LinuxVM001 adındaki bir Linux tabanlı sanal makineden ResourceGroup002 adındaki kaynak grubuna ait bir Chef uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="18ffc-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="18ffc-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18ffc-114">PARAMETERS</span></span>

### <span data-ttu-id="18ffc-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="18ffc-115">-Linux</span></span>
<span data-ttu-id="18ffc-116">Bu cmdlet 'in bir Linux sanal makinesini hedeflediği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="18ffc-116">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18ffc-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="18ffc-117">-Name</span></span>
<span data-ttu-id="18ffc-118">Bu cmdlet 'in kaldırıldığı Chef uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18ffc-118">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18ffc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18ffc-119">-ResourceGroupName</span></span>
<span data-ttu-id="18ffc-120">Sanal makineyi içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18ffc-120">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18ffc-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="18ffc-121">-VMName</span></span>
<span data-ttu-id="18ffc-122">Bu cmdlet 'in Chef uzantısını kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18ffc-122">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18ffc-123">-Windows</span><span class="sxs-lookup"><span data-stu-id="18ffc-123">-Windows</span></span>
<span data-ttu-id="18ffc-124">Bu cmdlet 'in Windows sanal makinesini hedeflediği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="18ffc-124">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18ffc-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="18ffc-125">-Confirm</span></span>
<span data-ttu-id="18ffc-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="18ffc-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18ffc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18ffc-127">-WhatIf</span></span>
<span data-ttu-id="18ffc-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="18ffc-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="18ffc-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="18ffc-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18ffc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18ffc-130">CommonParameters</span></span>
<span data-ttu-id="18ffc-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18ffc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18ffc-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18ffc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18ffc-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18ffc-133">INPUTS</span></span>

### <span data-ttu-id="18ffc-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="18ffc-134">None</span></span>
<span data-ttu-id="18ffc-135">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="18ffc-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="18ffc-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18ffc-136">OUTPUTS</span></span>

## <span data-ttu-id="18ffc-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18ffc-137">NOTES</span></span>

## <span data-ttu-id="18ffc-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18ffc-138">RELATED LINKS</span></span>

[<span data-ttu-id="18ffc-139">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="18ffc-139">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="18ffc-140">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="18ffc-140">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)
