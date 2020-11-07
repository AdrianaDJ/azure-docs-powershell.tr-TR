---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
ms.openlocfilehash: add3437794430e0d5e41ab9330072db4ac3e1616
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917444"
---
# <span data-ttu-id="c9ba0-101">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="c9ba0-101">Get-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="c9ba0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="c9ba0-103">Özel bir komut dosyası uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c9ba0-103">Gets information about a custom script extension.</span></span>

## <span data-ttu-id="c9ba0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9ba0-104">SYNTAX</span></span>

```
Get-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9ba0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9ba0-105">DESCRIPTION</span></span>
<span data-ttu-id="c9ba0-106">**Get-AzVMCustomScriptExtension** cmdlet 'i, bir sanal makinedeki özel betik sanal makine uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c9ba0-106">The **Get-AzVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="c9ba0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9ba0-107">EXAMPLES</span></span>

### <span data-ttu-id="c9ba0-108">Örnek 1: özel bir komut dosyası uzantısı alma</span><span class="sxs-lookup"><span data-stu-id="c9ba0-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="c9ba0-109">Bu komut, VirtualMachine07 adındaki sanal makine için ContosoCustomScript adındaki özel komut dosyası uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="c9ba0-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="c9ba0-110">Örnek 2: özel bir komut dosyası uzantısının örnek görünümünü alma</span><span class="sxs-lookup"><span data-stu-id="c9ba0-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="c9ba0-111">Bu komut, VirtualMachine07 adındaki sanal makine için ContosoCustomScript adındaki özel komut dosyası uzantısının örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="c9ba0-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="c9ba0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9ba0-112">PARAMETERS</span></span>

### <span data-ttu-id="c9ba0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9ba0-113">-DefaultProfile</span></span>
<span data-ttu-id="c9ba0-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c9ba0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9ba0-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="c9ba0-115">-Name</span></span>
<span data-ttu-id="c9ba0-116">Bu cmdlet 'in bilgi aldığı özel komut dosyası uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9ba0-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="c9ba0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9ba0-117">-ResourceGroupName</span></span>
<span data-ttu-id="c9ba0-118">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9ba0-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c9ba0-119">-Durum</span><span class="sxs-lookup"><span data-stu-id="c9ba0-119">-Status</span></span>
<span data-ttu-id="c9ba0-120">Bu cmdlet 'in özel betik uzantısının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9ba0-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="c9ba0-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="c9ba0-121">-VMName</span></span>
<span data-ttu-id="c9ba0-122">Bu cmdlet 'in özel komut dosyası uzantısını aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9ba0-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="c9ba0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9ba0-123">CommonParameters</span></span>
<span data-ttu-id="c9ba0-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9ba0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9ba0-125">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c9ba0-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9ba0-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9ba0-126">INPUTS</span></span>

### <span data-ttu-id="c9ba0-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c9ba0-127">System.String</span></span>

### <span data-ttu-id="c9ba0-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c9ba0-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c9ba0-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9ba0-129">OUTPUTS</span></span>

### <span data-ttu-id="c9ba0-130">Microsoft. Azure. Commands. COMPUTE. model. Virtualmachineccustomscriplersioncontext</span><span class="sxs-lookup"><span data-stu-id="c9ba0-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="c9ba0-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9ba0-131">NOTES</span></span>

## <span data-ttu-id="c9ba0-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9ba0-132">RELATED LINKS</span></span>

[<span data-ttu-id="c9ba0-133">Get-azvmaccessexten</span><span class="sxs-lookup"><span data-stu-id="c9ba0-133">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="c9ba0-134">Get-Azvmexgeri</span><span class="sxs-lookup"><span data-stu-id="c9ba0-134">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="c9ba0-135">Get-Azvmextensionımage</span><span class="sxs-lookup"><span data-stu-id="c9ba0-135">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


