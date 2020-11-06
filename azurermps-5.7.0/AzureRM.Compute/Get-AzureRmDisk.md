---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e34016b3bc7677c9591c07e54dd42a88a820d44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591068"
---
# <span data-ttu-id="785b5-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="785b5-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="785b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="785b5-102">SYNOPSIS</span></span>
<span data-ttu-id="785b5-103">Diskin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="785b5-103">Gets the properties of a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="785b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="785b5-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="785b5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="785b5-105">DESCRIPTION</span></span>
<span data-ttu-id="785b5-106">**Get-Azurermdısk** cmdlet 'i, bir diskin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="785b5-106">The **Get-AzureRmDisk** cmdlet gets the properties of a disk.</span></span>

## <span data-ttu-id="785b5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="785b5-107">EXAMPLES</span></span>

### <span data-ttu-id="785b5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="785b5-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="785b5-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Disk01 ' adındaki diskin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="785b5-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="785b5-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="785b5-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="785b5-111">Bu komut, ' ResourceGroup01 ' kaynak grubundaki tüm disklerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="785b5-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="785b5-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="785b5-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="785b5-113">Bu komut, aboneliğin altındaki tüm disklerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="785b5-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="785b5-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="785b5-114">PARAMETERS</span></span>

### <span data-ttu-id="785b5-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="785b5-115">-DiskName</span></span>
<span data-ttu-id="785b5-116">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="785b5-116">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="785b5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="785b5-117">-ResourceGroupName</span></span>
<span data-ttu-id="785b5-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="785b5-118">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="785b5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="785b5-119">CommonParameters</span></span>
<span data-ttu-id="785b5-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="785b5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="785b5-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="785b5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="785b5-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="785b5-122">INPUTS</span></span>

### <span data-ttu-id="785b5-123">System. String</span><span class="sxs-lookup"><span data-stu-id="785b5-123">System.String</span></span>

## <span data-ttu-id="785b5-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="785b5-124">OUTPUTS</span></span>

### <span data-ttu-id="785b5-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIşleç listesi</span><span class="sxs-lookup"><span data-stu-id="785b5-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList</span></span>

## <span data-ttu-id="785b5-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="785b5-126">NOTES</span></span>

## <span data-ttu-id="785b5-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="785b5-127">RELATED LINKS</span></span>

