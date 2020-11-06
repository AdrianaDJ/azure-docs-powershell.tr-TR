---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
ms.openlocfilehash: 5733939c24437c974f629588106d6240766a9df1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589880"
---
# <span data-ttu-id="990b2-101">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="990b2-101">Get-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="990b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="990b2-102">SYNOPSIS</span></span>
<span data-ttu-id="990b2-103">Bir Çef uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="990b2-103">Gets information about a Chef extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="990b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="990b2-104">SYNTAX</span></span>

### <span data-ttu-id="990b2-105">UX</span><span class="sxs-lookup"><span data-stu-id="990b2-105">Linux</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Linux] [<CommonParameters>]
```

### <span data-ttu-id="990b2-106">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="990b2-106">Windows</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Windows] [<CommonParameters>]
```

## <span data-ttu-id="990b2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="990b2-107">DESCRIPTION</span></span>
<span data-ttu-id="990b2-108">**Get-AzureVMChefExtension** cmdlet 'i sanal makinede yüklü bir Chef uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="990b2-108">The **Get-AzureVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="990b2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="990b2-109">EXAMPLES</span></span>

### <span data-ttu-id="990b2-110">Örnek 1: Windows sanal makinesi için Chef uzantısının ayrıntılarını alma-</span><span class="sxs-lookup"><span data-stu-id="990b2-110">Example 1: Get the details of Chef extension for a Windows virtual machine-</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="990b2-111">Bu komut, ResourceGroup001 adındaki kaynak grubuna ait olan WindowsVM001 adındaki bir Windows sanal makinesinden Chef uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="990b2-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="990b2-112">Örnek 2: Linux sanal makinesi için Chef uzantısının ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="990b2-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="990b2-113">Bu komut, LinuxVM001 adındaki bir Linux sanal makinesinden ResourceGroup002 adındaki kaynak grubuna ait Chef uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="990b2-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="990b2-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="990b2-114">PARAMETERS</span></span>

### <span data-ttu-id="990b2-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="990b2-115">-Linux</span></span>
<span data-ttu-id="990b2-116">Bu cmdlet 'in Linux sanal makinede çalıştığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="990b2-116">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

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

### <span data-ttu-id="990b2-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="990b2-117">-Name</span></span>
<span data-ttu-id="990b2-118">Chef uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="990b2-118">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="990b2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="990b2-119">-ResourceGroupName</span></span>
<span data-ttu-id="990b2-120">Sanal makineyi içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="990b2-120">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="990b2-121">-Durum</span><span class="sxs-lookup"><span data-stu-id="990b2-121">-Status</span></span>
<span data-ttu-id="990b2-122">Bu cmdlet 'in yalnızca Chef uzantısının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="990b2-122">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

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

### <span data-ttu-id="990b2-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="990b2-123">-VMName</span></span>
<span data-ttu-id="990b2-124">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="990b2-124">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="990b2-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="990b2-125">-Windows</span></span>
<span data-ttu-id="990b2-126">Bu cmdlet 'in bir Windows sanal makinesi için olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="990b2-126">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

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

### <span data-ttu-id="990b2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="990b2-127">CommonParameters</span></span>
<span data-ttu-id="990b2-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="990b2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="990b2-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="990b2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="990b2-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="990b2-130">INPUTS</span></span>

### <span data-ttu-id="990b2-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="990b2-131">None</span></span>
<span data-ttu-id="990b2-132">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="990b2-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="990b2-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="990b2-133">OUTPUTS</span></span>

## <span data-ttu-id="990b2-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="990b2-134">NOTES</span></span>

## <span data-ttu-id="990b2-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="990b2-135">RELATED LINKS</span></span>

[<span data-ttu-id="990b2-136">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="990b2-136">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)

[<span data-ttu-id="990b2-137">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="990b2-137">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)


