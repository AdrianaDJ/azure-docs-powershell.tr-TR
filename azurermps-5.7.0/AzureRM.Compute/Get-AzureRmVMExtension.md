---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
ms.openlocfilehash: 82ab2f02d47b17342f71b09eebe826fc48c07b81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587630"
---
# <span data-ttu-id="5b377-101">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="5b377-101">Get-AzureRmVMExtension</span></span>

## <span data-ttu-id="5b377-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b377-102">SYNOPSIS</span></span>
<span data-ttu-id="5b377-103">Sanal makinede yüklü sanal makine uzantılarının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="5b377-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b377-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b377-104">SYNTAX</span></span>

```
Get-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="5b377-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b377-105">DESCRIPTION</span></span>
<span data-ttu-id="5b377-106">**Get-Azurermvmexter** cmdlet 'i, sanal makinede yüklü sanal makine uzantılarının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="5b377-106">The **Get-AzureRmVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="5b377-107">Özelliklerini almak istediğiniz uzantının adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="5b377-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="5b377-108">Bir uzantının yalnızca örnek görünümüne ulaşmak için, durum parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="5b377-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="5b377-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b377-109">EXAMPLES</span></span>

### <span data-ttu-id="5b377-110">Örnek 1: bir uzantının özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="5b377-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="5b377-111">Bu komut ResourceGroup11 kaynak grubundaki VirtualMachine22 adındaki sanal makinede CustomScriptExtension adlı uzantının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="5b377-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="5b377-112">Örnek 2: uzantının örnek görünümünü alma</span><span class="sxs-lookup"><span data-stu-id="5b377-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="5b377-113">Bu komut, kaynak grubundaki ResourceGroup11 VirtualMachine22 adındaki sanal makinede CustomScriptExtension adlı uzantının örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="5b377-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="5b377-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b377-114">PARAMETERS</span></span>

### <span data-ttu-id="5b377-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="5b377-115">-Name</span></span>
<span data-ttu-id="5b377-116">Bir uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b377-116">Specifies the name of an extension.</span></span>
<span data-ttu-id="5b377-117">Bu cmdlet, bu parametrenin belirttiği uzantının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="5b377-117">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="5b377-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b377-118">-ResourceGroupName</span></span>
<span data-ttu-id="5b377-119">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b377-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5b377-120">-Durum</span><span class="sxs-lookup"><span data-stu-id="5b377-120">-Status</span></span>
<span data-ttu-id="5b377-121">Bu cmdlet 'in yalnızca bir uzantının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5b377-121">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="5b377-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="5b377-122">-VMName</span></span>
<span data-ttu-id="5b377-123">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b377-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="5b377-124">Bu cmdlet, bu parametrenin belirttiği sanal makineden uzantının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="5b377-124">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="5b377-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b377-125">CommonParameters</span></span>
<span data-ttu-id="5b377-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b377-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b377-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b377-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b377-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b377-128">INPUTS</span></span>

### <span data-ttu-id="5b377-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5b377-129">None</span></span>
<span data-ttu-id="5b377-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="5b377-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5b377-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b377-131">OUTPUTS</span></span>

## <span data-ttu-id="5b377-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b377-132">NOTES</span></span>

## <span data-ttu-id="5b377-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b377-133">RELATED LINKS</span></span>

[<span data-ttu-id="5b377-134">Remove-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="5b377-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)

[<span data-ttu-id="5b377-135">Set-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="5b377-135">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


