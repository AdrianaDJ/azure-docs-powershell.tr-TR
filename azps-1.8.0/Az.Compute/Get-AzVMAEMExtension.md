---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: 8cd67aa715b0092c82a3553158a4736d8f1e850e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917448"
---
# <span data-ttu-id="cc737-101">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cc737-101">Get-AzVMAEMExtension</span></span>

## <span data-ttu-id="cc737-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc737-102">SYNOPSIS</span></span>
<span data-ttu-id="cc737-103">AEM uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="cc737-103">Gets information about the AEM extension.</span></span>

## <span data-ttu-id="cc737-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cc737-104">SYNTAX</span></span>

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc737-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cc737-105">DESCRIPTION</span></span>
<span data-ttu-id="cc737-106">**Get-AzVMAEMExtension** cmdlet 'ı, Azure Gelişmiş izleme (AEM) uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="cc737-106">The **Get-AzVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="cc737-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cc737-107">EXAMPLES</span></span>

### <span data-ttu-id="cc737-108">Örnek 1: AEM uzantısını alma</span><span class="sxs-lookup"><span data-stu-id="cc737-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="cc737-109">Bu komut contoso-Server adlı sanal makinenin AEM uzantısı için bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="cc737-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="cc737-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cc737-110">PARAMETERS</span></span>

### <span data-ttu-id="cc737-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc737-111">-DefaultProfile</span></span>
<span data-ttu-id="cc737-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cc737-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc737-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="cc737-113">-Name</span></span>
<span data-ttu-id="cc737-114">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc737-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="cc737-115">Bu cmdlet, bu cmdlet 'in belirttiği sanal makinedeki AEM uzantısı için bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="cc737-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="cc737-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="cc737-116">-OSType</span></span>
<span data-ttu-id="cc737-117">İşletim sistemi diskinin işletim sisteminin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc737-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="cc737-118">İşletim sistemi diskinin türü yoksa, bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cc737-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="cc737-119">Bu parametre için kabul edilebilir değerler: Windows ve Linux.</span><span class="sxs-lookup"><span data-stu-id="cc737-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc737-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc737-120">-ResourceGroupName</span></span>
<span data-ttu-id="cc737-121">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc737-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="cc737-122">Bu cmdlet, bu sanal makinedeki AEM uzantısı için bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="cc737-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="cc737-123">-Durum</span><span class="sxs-lookup"><span data-stu-id="cc737-123">-Status</span></span>
<span data-ttu-id="cc737-124">Bu cmdlet 'in yalnızca AEM uzantısının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cc737-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

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

### <span data-ttu-id="cc737-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="cc737-125">-VMName</span></span>
<span data-ttu-id="cc737-126">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc737-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="cc737-127">Bu cmdlet, bu parametrenin belirttiği sanal makinenin AEM uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="cc737-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="cc737-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc737-128">CommonParameters</span></span>
<span data-ttu-id="cc737-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cc737-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc737-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cc737-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc737-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cc737-131">INPUTS</span></span>

### <span data-ttu-id="cc737-132">System. String</span><span class="sxs-lookup"><span data-stu-id="cc737-132">System.String</span></span>

### <span data-ttu-id="cc737-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cc737-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cc737-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cc737-134">OUTPUTS</span></span>

### <span data-ttu-id="cc737-135">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="cc737-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="cc737-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cc737-136">NOTES</span></span>

## <span data-ttu-id="cc737-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cc737-137">RELATED LINKS</span></span>

[<span data-ttu-id="cc737-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cc737-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="cc737-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cc737-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="cc737-140">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cc737-140">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)

