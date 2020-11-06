---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 9f4d2c4e6321d36079cf4c5e87747863c8dc51c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591064"
---
# <span data-ttu-id="714d1-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="714d1-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="714d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="714d1-102">SYNOPSIS</span></span>
<span data-ttu-id="714d1-103">Anlık görüntünün özelliklerini alır</span><span class="sxs-lookup"><span data-stu-id="714d1-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="714d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="714d1-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="714d1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="714d1-105">DESCRIPTION</span></span>
<span data-ttu-id="714d1-106">**Get-AzureRmSnapshot** cmdlet 'inin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="714d1-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="714d1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="714d1-107">EXAMPLES</span></span>

### <span data-ttu-id="714d1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="714d1-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="714d1-109">Bu komut, aboneliğin tüm anlık görüntülerinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="714d1-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="714d1-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="714d1-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="714d1-111">Bu komut, "ResourceGroupName1" adlı kaynak grubundaki tüm anlık görüntülerin özelliklerini alır</span><span class="sxs-lookup"><span data-stu-id="714d1-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="714d1-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="714d1-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="714d1-113">Bu komut, "ResourceGroupName1" adlı kaynak grubundaki "SnapshotName1" adlı anlık görüntünün özelliklerini alır</span><span class="sxs-lookup"><span data-stu-id="714d1-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="714d1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="714d1-114">PARAMETERS</span></span>

### <span data-ttu-id="714d1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="714d1-115">-ResourceGroupName</span></span>
<span data-ttu-id="714d1-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="714d1-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="714d1-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="714d1-117">-SnapshotName</span></span>
<span data-ttu-id="714d1-118">Anlık görüntünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="714d1-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="714d1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="714d1-119">CommonParameters</span></span>
<span data-ttu-id="714d1-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="714d1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="714d1-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="714d1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="714d1-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="714d1-122">INPUTS</span></span>

### <span data-ttu-id="714d1-123">System. String</span><span class="sxs-lookup"><span data-stu-id="714d1-123">System.String</span></span>

## <span data-ttu-id="714d1-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="714d1-124">OUTPUTS</span></span>

### <span data-ttu-id="714d1-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="714d1-125">System.Object</span></span>

## <span data-ttu-id="714d1-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="714d1-126">NOTES</span></span>

## <span data-ttu-id="714d1-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="714d1-127">RELATED LINKS</span></span>

