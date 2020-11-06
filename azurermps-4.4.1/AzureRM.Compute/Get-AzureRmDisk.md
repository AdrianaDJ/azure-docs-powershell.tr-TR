---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e598c266f46815e7005c43e2d354ad8ece06efc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594308"
---
# <span data-ttu-id="c7442-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="c7442-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="c7442-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7442-102">SYNOPSIS</span></span>
<span data-ttu-id="c7442-103">Diskin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="c7442-103">Gets the properties of a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7442-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7442-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7442-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7442-105">DESCRIPTION</span></span>
<span data-ttu-id="c7442-106">**Get-Azurermdısk** cmdlet 'i, bir diskin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="c7442-106">The **Get-AzureRmDisk** cmdlet gets the properties of a disk.</span></span>

## <span data-ttu-id="c7442-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7442-107">EXAMPLES</span></span>

### <span data-ttu-id="c7442-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c7442-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="c7442-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Disk01 ' adındaki diskin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="c7442-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="c7442-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c7442-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="c7442-111">Bu komut, ' ResourceGroup01 ' kaynak grubundaki tüm disklerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="c7442-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="c7442-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c7442-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="c7442-113">Bu komut, aboneliğin altındaki tüm disklerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="c7442-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="c7442-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7442-114">PARAMETERS</span></span>

### <span data-ttu-id="c7442-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7442-115">-DefaultProfile</span></span>
<span data-ttu-id="c7442-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c7442-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7442-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="c7442-117">-DiskName</span></span>
<span data-ttu-id="c7442-118">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7442-118">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7442-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7442-119">-ResourceGroupName</span></span>
<span data-ttu-id="c7442-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7442-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7442-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7442-121">CommonParameters</span></span>
<span data-ttu-id="c7442-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7442-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7442-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7442-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7442-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7442-124">INPUTS</span></span>

### <span data-ttu-id="c7442-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c7442-125">System.String</span></span>

## <span data-ttu-id="c7442-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7442-126">OUTPUTS</span></span>

### <span data-ttu-id="c7442-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="c7442-127">System.Object</span></span>

## <span data-ttu-id="c7442-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7442-128">NOTES</span></span>

## <span data-ttu-id="c7442-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7442-129">RELATED LINKS</span></span>

