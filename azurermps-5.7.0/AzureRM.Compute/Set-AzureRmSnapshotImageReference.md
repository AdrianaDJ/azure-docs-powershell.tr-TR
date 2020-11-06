---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotImageReference.md
ms.openlocfilehash: 262184f82aa169b5e76d3b875d0e3ba27db4da38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586788"
---
# <span data-ttu-id="076c0-101">Set-AzureRmSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="076c0-101">Set-AzureRmSnapshotImageReference</span></span>

## <span data-ttu-id="076c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="076c0-102">SYNOPSIS</span></span>
<span data-ttu-id="076c0-103">Anlık görüntü nesnesinde görüntü başvurusu özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="076c0-103">Sets the image reference properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="076c0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="076c0-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotImageReference [-Snapshot] <Snapshot> [[-Id] <String>] [[-Lun] <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="076c0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="076c0-105">DESCRIPTION</span></span>
<span data-ttu-id="076c0-106">**Set-Azurermsnapshotıgereference** cmdlet 'i, anlık görüntü nesnesinde görüntü başvurusu özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="076c0-106">The **Set-AzureRmSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="076c0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="076c0-107">EXAMPLES</span></span>

### <span data-ttu-id="076c0-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="076c0-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzureRmSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="076c0-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 GB olan yerel bir anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="076c0-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="076c0-110">Ayrıca Windows işletim sistemi türünü de ayarlar.</span><span class="sxs-lookup"><span data-stu-id="076c0-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="076c0-111">İkinci komut, anlık görüntü nesnesinin görüntü KIMLIĞINI ve 0 mantıksal birim sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="076c0-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="076c0-112">Son komut, Snapshot nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adıyla bir anlık görüntü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="076c0-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="076c0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="076c0-113">PARAMETERS</span></span>

### <span data-ttu-id="076c0-114">-ID</span><span class="sxs-lookup"><span data-stu-id="076c0-114">-Id</span></span>
<span data-ttu-id="076c0-115">KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="076c0-115">Specifies the ID.</span></span>

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

### <span data-ttu-id="076c0-116">-LUN</span><span class="sxs-lookup"><span data-stu-id="076c0-116">-Lun</span></span>
<span data-ttu-id="076c0-117">Mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="076c0-117">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="076c0-118">-Anlık görüntü</span><span class="sxs-lookup"><span data-stu-id="076c0-118">-Snapshot</span></span>
<span data-ttu-id="076c0-119">Yerel bir anlık görüntü nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="076c0-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="076c0-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="076c0-120">-Confirm</span></span>
<span data-ttu-id="076c0-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="076c0-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="076c0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="076c0-122">-WhatIf</span></span>
<span data-ttu-id="076c0-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="076c0-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="076c0-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="076c0-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="076c0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="076c0-125">CommonParameters</span></span>
<span data-ttu-id="076c0-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="076c0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="076c0-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="076c0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="076c0-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="076c0-128">INPUTS</span></span>

### <span data-ttu-id="076c0-129">Microsoft. Azure. Management. COMPUTE. modeller. anlık görüntüsü</span><span class="sxs-lookup"><span data-stu-id="076c0-129">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="076c0-130">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="076c0-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="076c0-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="076c0-131">OUTPUTS</span></span>

### <span data-ttu-id="076c0-132">Microsoft. Azure. Management. COMPUTE. modeller. anlık görüntüsü</span><span class="sxs-lookup"><span data-stu-id="076c0-132">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="076c0-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="076c0-133">NOTES</span></span>

## <span data-ttu-id="076c0-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="076c0-134">RELATED LINKS</span></span>

