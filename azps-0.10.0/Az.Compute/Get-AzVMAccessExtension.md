---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: 23120c9225d6905a528ac113bd055ec8fa585870
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937038"
---
# <span data-ttu-id="9101b-101">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="9101b-101">Get-AzVMAccessExtension</span></span>

## <span data-ttu-id="9101b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9101b-102">SYNOPSIS</span></span>
<span data-ttu-id="9101b-103">VMAccess uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="9101b-103">Gets information about the VMAccess extension.</span></span>

## <span data-ttu-id="9101b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9101b-104">SYNTAX</span></span>

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9101b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9101b-105">DESCRIPTION</span></span>
<span data-ttu-id="9101b-106">**Get-Azvmaccessextenma** cmdlet 'ı sanal makine erişimi (VMAccess) sanal makine uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="9101b-106">The **Get-AzVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="9101b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9101b-107">EXAMPLES</span></span>

### <span data-ttu-id="9101b-108">Örnek 1: VMAccess uzantısını alma</span><span class="sxs-lookup"><span data-stu-id="9101b-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="9101b-109">Bu komut, VirtualMachine07 adındaki sanal makine için ContosoTest adındaki VMAccess uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="9101b-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="9101b-110">Örnek 2: VMAccess uzantısının örnek görünümünü alma</span><span class="sxs-lookup"><span data-stu-id="9101b-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="9101b-111">Bu komut, VirtualMachine07 adındaki sanal makine için ContosoTest adındaki VMAccess uzantısının örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="9101b-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="9101b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9101b-112">PARAMETERS</span></span>

### <span data-ttu-id="9101b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9101b-113">-DefaultProfile</span></span>
<span data-ttu-id="9101b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9101b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9101b-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="9101b-115">-Name</span></span>
<span data-ttu-id="9101b-116">Bu cmdlet 'in aldığı uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9101b-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9101b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9101b-117">-ResourceGroupName</span></span>
<span data-ttu-id="9101b-118">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9101b-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9101b-119">-Durum</span><span class="sxs-lookup"><span data-stu-id="9101b-119">-Status</span></span>
<span data-ttu-id="9101b-120">Bu cmdlet 'in yalnızca uzantının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9101b-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="9101b-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="9101b-121">-VMName</span></span>
<span data-ttu-id="9101b-122">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9101b-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="9101b-123">Bu cmdlet, bu parametrenin belirttiği sanal makinede VMAccess hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="9101b-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="9101b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9101b-124">CommonParameters</span></span>
<span data-ttu-id="9101b-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9101b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9101b-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9101b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9101b-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9101b-127">INPUTS</span></span>

### <span data-ttu-id="9101b-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9101b-128">None</span></span>
<span data-ttu-id="9101b-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="9101b-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9101b-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9101b-130">OUTPUTS</span></span>

### <span data-ttu-id="9101b-131">Microsoft. Azure. Commands. COMPUTE. modeller. VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="9101b-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="9101b-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9101b-132">NOTES</span></span>

## <span data-ttu-id="9101b-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9101b-133">RELATED LINKS</span></span>

[<span data-ttu-id="9101b-134">Remove-azvmaccessexten</span><span class="sxs-lookup"><span data-stu-id="9101b-134">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="9101b-135">Set-azvmaccessexten</span><span class="sxs-lookup"><span data-stu-id="9101b-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="9101b-136">Get-Azvmexgeri</span><span class="sxs-lookup"><span data-stu-id="9101b-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)


