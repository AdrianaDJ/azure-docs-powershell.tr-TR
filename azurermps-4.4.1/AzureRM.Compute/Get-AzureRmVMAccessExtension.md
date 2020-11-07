---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
ms.openlocfilehash: f5ba6ede0b57d2480a892efd47ed71aacd9fe553
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595202"
---
# <span data-ttu-id="c0c7b-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="c0c7b-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="c0c7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0c7b-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c7b-103">VMAccess uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0c7b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0c7b-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0c7b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0c7b-105">DESCRIPTION</span></span>
<span data-ttu-id="c0c7b-106">**Get-Azurermvmaccessextenma** cmdlet 'ı sanal makine erişimi (VMAccess) sanal makine uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="c0c7b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0c7b-107">EXAMPLES</span></span>

### <span data-ttu-id="c0c7b-108">Örnek 1: VMAccess uzantısını alma</span><span class="sxs-lookup"><span data-stu-id="c0c7b-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="c0c7b-109">Bu komut, VirtualMachine07 adındaki sanal makine için ContosoTest adındaki VMAccess uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="c0c7b-110">Örnek 2: VMAccess uzantısının örnek görünümünü alma</span><span class="sxs-lookup"><span data-stu-id="c0c7b-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="c0c7b-111">Bu komut, VirtualMachine07 adındaki sanal makine için ContosoTest adındaki VMAccess uzantısının örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="c0c7b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0c7b-112">PARAMETERS</span></span>

### <span data-ttu-id="c0c7b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c7b-113">-DefaultProfile</span></span>
<span data-ttu-id="c0c7b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0c7b-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="c0c7b-115">-Name</span></span>
<span data-ttu-id="c0c7b-116">Bu cmdlet 'in aldığı uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c0c7b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0c7b-117">-ResourceGroupName</span></span>
<span data-ttu-id="c0c7b-118">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c0c7b-119">-Durum</span><span class="sxs-lookup"><span data-stu-id="c0c7b-119">-Status</span></span>
<span data-ttu-id="c0c7b-120">Bu cmdlet 'in yalnızca uzantının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="c0c7b-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="c0c7b-121">-VMName</span></span>
<span data-ttu-id="c0c7b-122">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="c0c7b-123">Bu cmdlet, bu parametrenin belirttiği sanal makinede VMAccess hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="c0c7b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c7b-124">CommonParameters</span></span>
<span data-ttu-id="c0c7b-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c7b-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0c7b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c7b-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0c7b-127">INPUTS</span></span>

## <span data-ttu-id="c0c7b-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0c7b-128">OUTPUTS</span></span>

## <span data-ttu-id="c0c7b-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0c7b-129">NOTES</span></span>

## <span data-ttu-id="c0c7b-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0c7b-130">RELATED LINKS</span></span>

[<span data-ttu-id="c0c7b-131">Remove-Azurermvmaccessextenma</span><span class="sxs-lookup"><span data-stu-id="c0c7b-131">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="c0c7b-132">Set-Azurermvmaccessextenma</span><span class="sxs-lookup"><span data-stu-id="c0c7b-132">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="c0c7b-133">Get-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="c0c7b-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

