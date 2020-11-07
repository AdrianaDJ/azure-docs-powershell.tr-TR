---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzSnapshot.md
ms.openlocfilehash: 25395cca287e7f711d5e124ab12919a0b5c01ce4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937052"
---
# <span data-ttu-id="ba104-101">Get-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="ba104-101">Get-AzSnapshot</span></span>

## <span data-ttu-id="ba104-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba104-102">SYNOPSIS</span></span>
<span data-ttu-id="ba104-103">Anlık görüntünün özelliklerini alır</span><span class="sxs-lookup"><span data-stu-id="ba104-103">Gets the properties of a snapshot</span></span>

## <span data-ttu-id="ba104-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba104-104">SYNTAX</span></span>

```
Get-AzSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba104-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba104-105">DESCRIPTION</span></span>
<span data-ttu-id="ba104-106">**Get-azsnapshot** cmdlet 'inin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="ba104-106">The **Get-AzSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="ba104-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba104-107">EXAMPLES</span></span>

### <span data-ttu-id="ba104-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ba104-108">Example 1</span></span>
```
PS C:\> Get-AzSnapshot
```

<span data-ttu-id="ba104-109">Bu komut, aboneliğin tüm anlık görüntülerinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="ba104-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="ba104-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ba104-110">Example 2</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="ba104-111">Bu komut, "ResourceGroupName1" adlı kaynak grubundaki tüm anlık görüntülerin özelliklerini alır</span><span class="sxs-lookup"><span data-stu-id="ba104-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="ba104-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="ba104-112">Example 3</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="ba104-113">Bu komut, "ResourceGroupName1" adlı kaynak grubundaki "SnapshotName1" adlı anlık görüntünün özelliklerini alır</span><span class="sxs-lookup"><span data-stu-id="ba104-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="ba104-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba104-114">PARAMETERS</span></span>

### <span data-ttu-id="ba104-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba104-115">-DefaultProfile</span></span>
<span data-ttu-id="ba104-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ba104-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba104-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba104-117">-ResourceGroupName</span></span>
<span data-ttu-id="ba104-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba104-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ba104-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="ba104-119">-SnapshotName</span></span>
<span data-ttu-id="ba104-120">Anlık görüntünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba104-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="ba104-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba104-121">CommonParameters</span></span>
<span data-ttu-id="ba104-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba104-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba104-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba104-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba104-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba104-124">INPUTS</span></span>

### <span data-ttu-id="ba104-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ba104-125">System.String</span></span>

## <span data-ttu-id="ba104-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba104-126">OUTPUTS</span></span>

### <span data-ttu-id="ba104-127">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="ba104-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="ba104-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba104-128">NOTES</span></span>

## <span data-ttu-id="ba104-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba104-129">RELATED LINKS</span></span>

