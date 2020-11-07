---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
ms.openlocfilehash: 889bd206566b9c722aa187f9e32a76c1711af337
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762316"
---
# <span data-ttu-id="80ba2-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="80ba2-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="80ba2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80ba2-102">SYNOPSIS</span></span>
<span data-ttu-id="80ba2-103">VMAccess uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="80ba2-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80ba2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="80ba2-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80ba2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="80ba2-105">DESCRIPTION</span></span>
<span data-ttu-id="80ba2-106">**Get-Azurermvmaccessextenma** cmdlet 'ı sanal makine erişimi (VMAccess) sanal makine uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="80ba2-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="80ba2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="80ba2-107">EXAMPLES</span></span>

### <span data-ttu-id="80ba2-108">Örnek 1: VMAccess uzantısını alma</span><span class="sxs-lookup"><span data-stu-id="80ba2-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="80ba2-109">Bu komut, VirtualMachine07 adındaki sanal makine için ContosoTest adındaki VMAccess uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="80ba2-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="80ba2-110">Örnek 2: VMAccess uzantısının örnek görünümünü alma</span><span class="sxs-lookup"><span data-stu-id="80ba2-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="80ba2-111">Bu komut, VirtualMachine07 adındaki sanal makine için ContosoTest adındaki VMAccess uzantısının örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="80ba2-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="80ba2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="80ba2-112">PARAMETERS</span></span>

### <span data-ttu-id="80ba2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80ba2-113">-DefaultProfile</span></span>
<span data-ttu-id="80ba2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="80ba2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80ba2-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="80ba2-115">-Name</span></span>
<span data-ttu-id="80ba2-116">Bu cmdlet 'in aldığı uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="80ba2-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="80ba2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80ba2-117">-ResourceGroupName</span></span>
<span data-ttu-id="80ba2-118">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="80ba2-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="80ba2-119">-Durum</span><span class="sxs-lookup"><span data-stu-id="80ba2-119">-Status</span></span>
<span data-ttu-id="80ba2-120">Bu cmdlet 'in yalnızca uzantının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="80ba2-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="80ba2-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="80ba2-121">-VMName</span></span>
<span data-ttu-id="80ba2-122">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="80ba2-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="80ba2-123">Bu cmdlet, bu parametrenin belirttiği sanal makinede VMAccess hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="80ba2-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="80ba2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80ba2-124">CommonParameters</span></span>
<span data-ttu-id="80ba2-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="80ba2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80ba2-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80ba2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80ba2-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="80ba2-127">INPUTS</span></span>

### <span data-ttu-id="80ba2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="80ba2-128">System.String</span></span>

### <span data-ttu-id="80ba2-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="80ba2-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="80ba2-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="80ba2-130">OUTPUTS</span></span>

### <span data-ttu-id="80ba2-131">Microsoft. Azure. Commands. COMPUTE. modeller. VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="80ba2-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="80ba2-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="80ba2-132">NOTES</span></span>

## <span data-ttu-id="80ba2-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="80ba2-133">RELATED LINKS</span></span>

[<span data-ttu-id="80ba2-134">Remove-Azurermvmaccessextenma</span><span class="sxs-lookup"><span data-stu-id="80ba2-134">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="80ba2-135">Set-Azurermvmaccessextenma</span><span class="sxs-lookup"><span data-stu-id="80ba2-135">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="80ba2-136">Get-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="80ba2-136">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

