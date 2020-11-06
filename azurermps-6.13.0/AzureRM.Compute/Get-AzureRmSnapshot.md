---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 14b1c1179e9fee15f398c4518e446cf47396e660
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588556"
---
# <span data-ttu-id="f7ae3-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="f7ae3-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="f7ae3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7ae3-102">SYNOPSIS</span></span>
<span data-ttu-id="f7ae3-103">Anlık görüntünün özelliklerini alır</span><span class="sxs-lookup"><span data-stu-id="f7ae3-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7ae3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f7ae3-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7ae3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7ae3-105">DESCRIPTION</span></span>
<span data-ttu-id="f7ae3-106">**Get-AzureRmSnapshot** cmdlet 'inin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="f7ae3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f7ae3-107">EXAMPLES</span></span>

### <span data-ttu-id="f7ae3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f7ae3-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="f7ae3-109">Bu komut, aboneliğin tüm anlık görüntülerinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="f7ae3-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f7ae3-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="f7ae3-111">Bu komut, "ResourceGroupName1" adlı kaynak grubundaki tüm anlık görüntülerin özelliklerini alır</span><span class="sxs-lookup"><span data-stu-id="f7ae3-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="f7ae3-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="f7ae3-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="f7ae3-113">Bu komut, "ResourceGroupName1" adlı kaynak grubundaki "SnapshotName1" adlı anlık görüntünün özelliklerini alır</span><span class="sxs-lookup"><span data-stu-id="f7ae3-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="f7ae3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f7ae3-114">PARAMETERS</span></span>

### <span data-ttu-id="f7ae3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7ae3-115">-DefaultProfile</span></span>
<span data-ttu-id="f7ae3-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7ae3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7ae3-117">-ResourceGroupName</span></span>
<span data-ttu-id="f7ae3-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f7ae3-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="f7ae3-119">-SnapshotName</span></span>
<span data-ttu-id="f7ae3-120">Anlık görüntünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="f7ae3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7ae3-121">CommonParameters</span></span>
<span data-ttu-id="f7ae3-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f7ae3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7ae3-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7ae3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7ae3-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f7ae3-124">INPUTS</span></span>

### <span data-ttu-id="f7ae3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f7ae3-125">System.String</span></span>

## <span data-ttu-id="f7ae3-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f7ae3-126">OUTPUTS</span></span>

### <span data-ttu-id="f7ae3-127">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="f7ae3-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="f7ae3-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f7ae3-128">NOTES</span></span>

## <span data-ttu-id="f7ae3-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f7ae3-129">RELATED LINKS</span></span>
