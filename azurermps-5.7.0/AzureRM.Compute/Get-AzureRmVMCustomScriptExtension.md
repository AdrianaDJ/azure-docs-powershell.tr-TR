---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 1f348a7cddc31a2a3d3d255aa6b4fe80d1808f36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589877"
---
# <span data-ttu-id="010d1-101">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="010d1-101">Get-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="010d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="010d1-102">SYNOPSIS</span></span>
<span data-ttu-id="010d1-103">Özel bir komut dosyası uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="010d1-103">Gets information about a custom script extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="010d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="010d1-104">SYNTAX</span></span>

```
Get-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="010d1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="010d1-105">DESCRIPTION</span></span>
<span data-ttu-id="010d1-106">**Get-AzureRmVMCustomScriptExtension** cmdlet 'i, bir sanal makinedeki özel betik sanal makine uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="010d1-106">The **Get-AzureRmVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="010d1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="010d1-107">EXAMPLES</span></span>

### <span data-ttu-id="010d1-108">Örnek 1: özel bir komut dosyası uzantısı alma</span><span class="sxs-lookup"><span data-stu-id="010d1-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="010d1-109">Bu komut, VirtualMachine07 adındaki sanal makine için ContosoCustomScript adındaki özel komut dosyası uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="010d1-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="010d1-110">Örnek 2: özel bir komut dosyası uzantısının örnek görünümünü alma</span><span class="sxs-lookup"><span data-stu-id="010d1-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="010d1-111">Bu komut, VirtualMachine07 adındaki sanal makine için ContosoCustomScript adındaki özel komut dosyası uzantısının örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="010d1-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="010d1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="010d1-112">PARAMETERS</span></span>

### <span data-ttu-id="010d1-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="010d1-113">-Name</span></span>
<span data-ttu-id="010d1-114">Bu cmdlet 'in bilgi aldığı özel komut dosyası uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="010d1-114">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="010d1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="010d1-115">-ResourceGroupName</span></span>
<span data-ttu-id="010d1-116">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="010d1-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="010d1-117">-Durum</span><span class="sxs-lookup"><span data-stu-id="010d1-117">-Status</span></span>
<span data-ttu-id="010d1-118">Bu cmdlet 'in özel betik uzantısının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="010d1-118">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="010d1-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="010d1-119">-VMName</span></span>
<span data-ttu-id="010d1-120">Bu cmdlet 'in özel komut dosyası uzantısını aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="010d1-120">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="010d1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="010d1-121">CommonParameters</span></span>
<span data-ttu-id="010d1-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="010d1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="010d1-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="010d1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="010d1-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="010d1-124">INPUTS</span></span>

### <span data-ttu-id="010d1-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="010d1-125">None</span></span>
<span data-ttu-id="010d1-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="010d1-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="010d1-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="010d1-127">OUTPUTS</span></span>

## <span data-ttu-id="010d1-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="010d1-128">NOTES</span></span>

## <span data-ttu-id="010d1-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="010d1-129">RELATED LINKS</span></span>

[<span data-ttu-id="010d1-130">Get-Azurermvmaccessextenma</span><span class="sxs-lookup"><span data-stu-id="010d1-130">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="010d1-131">Get-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="010d1-131">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="010d1-132">Get-Azurermvmextensionımage</span><span class="sxs-lookup"><span data-stu-id="010d1-132">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


