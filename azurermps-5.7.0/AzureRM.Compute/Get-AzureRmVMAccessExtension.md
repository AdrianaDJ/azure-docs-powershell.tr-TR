---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
ms.openlocfilehash: 9e7cb85bf29d6982271768af6948db1d3c5b8605
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588982"
---
# <span data-ttu-id="43997-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="43997-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="43997-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43997-102">SYNOPSIS</span></span>
<span data-ttu-id="43997-103">VMAccess uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="43997-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43997-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="43997-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="43997-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="43997-105">DESCRIPTION</span></span>
<span data-ttu-id="43997-106">**Get-Azurermvmaccessextenma** cmdlet 'ı sanal makine erişimi (VMAccess) sanal makine uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="43997-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="43997-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="43997-107">EXAMPLES</span></span>

### <span data-ttu-id="43997-108">Örnek 1: VMAccess uzantısını alma</span><span class="sxs-lookup"><span data-stu-id="43997-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="43997-109">Bu komut, VirtualMachine07 adındaki sanal makine için ContosoTest adındaki VMAccess uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="43997-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="43997-110">Örnek 2: VMAccess uzantısının örnek görünümünü alma</span><span class="sxs-lookup"><span data-stu-id="43997-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="43997-111">Bu komut, VirtualMachine07 adındaki sanal makine için ContosoTest adındaki VMAccess uzantısının örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="43997-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="43997-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="43997-112">PARAMETERS</span></span>

### <span data-ttu-id="43997-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="43997-113">-Name</span></span>
<span data-ttu-id="43997-114">Bu cmdlet 'in aldığı uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43997-114">Specifies the name of the extension that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43997-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43997-115">-ResourceGroupName</span></span>
<span data-ttu-id="43997-116">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43997-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="43997-117">-Durum</span><span class="sxs-lookup"><span data-stu-id="43997-117">-Status</span></span>
<span data-ttu-id="43997-118">Bu cmdlet 'in yalnızca uzantının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="43997-118">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43997-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="43997-119">-VMName</span></span>
<span data-ttu-id="43997-120">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43997-120">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="43997-121">Bu cmdlet, bu parametrenin belirttiği sanal makinede VMAccess hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="43997-121">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="43997-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43997-122">CommonParameters</span></span>
<span data-ttu-id="43997-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="43997-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43997-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43997-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43997-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="43997-125">INPUTS</span></span>

### <span data-ttu-id="43997-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="43997-126">None</span></span>
<span data-ttu-id="43997-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="43997-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="43997-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="43997-128">OUTPUTS</span></span>

## <span data-ttu-id="43997-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="43997-129">NOTES</span></span>

## <span data-ttu-id="43997-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="43997-130">RELATED LINKS</span></span>

[<span data-ttu-id="43997-131">Remove-Azurermvmaccessextenma</span><span class="sxs-lookup"><span data-stu-id="43997-131">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="43997-132">Set-Azurermvmaccessextenma</span><span class="sxs-lookup"><span data-stu-id="43997-132">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="43997-133">Get-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="43997-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


