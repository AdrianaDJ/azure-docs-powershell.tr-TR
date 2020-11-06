---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtension.md
ms.openlocfilehash: 4aaee403007561797614b2534e29c5918dad3643
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592780"
---
# <span data-ttu-id="6b47d-101">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="6b47d-101">Get-AzureRmVMExtension</span></span>

## <span data-ttu-id="6b47d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b47d-102">SYNOPSIS</span></span>
<span data-ttu-id="6b47d-103">Sanal makinede yüklü sanal makine uzantılarının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6b47d-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b47d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b47d-104">SYNTAX</span></span>

```
Get-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b47d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b47d-105">DESCRIPTION</span></span>
<span data-ttu-id="6b47d-106">**Get-Azurermvmexter** cmdlet 'i, sanal makinede yüklü sanal makine uzantılarının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6b47d-106">The **Get-AzureRmVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="6b47d-107">Özelliklerini almak istediğiniz uzantının adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="6b47d-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="6b47d-108">Bir uzantının yalnızca örnek görünümüne ulaşmak için, durum parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="6b47d-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="6b47d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b47d-109">EXAMPLES</span></span>

### <span data-ttu-id="6b47d-110">Örnek 1: bir uzantının özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="6b47d-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="6b47d-111">Bu komut ResourceGroup11 kaynak grubundaki VirtualMachine22 adındaki sanal makinede CustomScriptExtension adlı uzantının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6b47d-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="6b47d-112">Örnek 2: uzantının örnek görünümünü alma</span><span class="sxs-lookup"><span data-stu-id="6b47d-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="6b47d-113">Bu komut, kaynak grubundaki ResourceGroup11 VirtualMachine22 adındaki sanal makinede CustomScriptExtension adlı uzantının örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="6b47d-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="6b47d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b47d-114">PARAMETERS</span></span>

### <span data-ttu-id="6b47d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b47d-115">-DefaultProfile</span></span>
<span data-ttu-id="6b47d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6b47d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b47d-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="6b47d-117">-Name</span></span>
<span data-ttu-id="6b47d-118">Bir uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b47d-118">Specifies the name of an extension.</span></span>
<span data-ttu-id="6b47d-119">Bu cmdlet, bu parametrenin belirttiği uzantının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6b47d-119">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="6b47d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b47d-120">-ResourceGroupName</span></span>
<span data-ttu-id="6b47d-121">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b47d-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6b47d-122">-Durum</span><span class="sxs-lookup"><span data-stu-id="6b47d-122">-Status</span></span>
<span data-ttu-id="6b47d-123">Bu cmdlet 'in yalnızca bir uzantının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b47d-123">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="6b47d-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="6b47d-124">-VMName</span></span>
<span data-ttu-id="6b47d-125">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b47d-125">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="6b47d-126">Bu cmdlet, bu parametrenin belirttiği sanal makineden uzantının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6b47d-126">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="6b47d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b47d-127">CommonParameters</span></span>
<span data-ttu-id="6b47d-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b47d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b47d-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b47d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b47d-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b47d-130">INPUTS</span></span>

### <span data-ttu-id="6b47d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6b47d-131">System.String</span></span>

### <span data-ttu-id="6b47d-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6b47d-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6b47d-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b47d-133">OUTPUTS</span></span>

### <span data-ttu-id="6b47d-134">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="6b47d-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="6b47d-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b47d-135">NOTES</span></span>

## <span data-ttu-id="6b47d-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b47d-136">RELATED LINKS</span></span>

[<span data-ttu-id="6b47d-137">Remove-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="6b47d-137">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)

[<span data-ttu-id="6b47d-138">Set-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="6b47d-138">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


