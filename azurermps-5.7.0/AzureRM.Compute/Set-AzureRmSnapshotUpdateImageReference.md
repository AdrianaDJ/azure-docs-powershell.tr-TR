---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
ms.openlocfilehash: fa6b3e16fd137453229232405d31cd7665ccd18e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587606"
---
# <span data-ttu-id="a02c7-101">Set-AzureRmSnapshotUpdateImageReference</span><span class="sxs-lookup"><span data-stu-id="a02c7-101">Set-AzureRmSnapshotUpdateImageReference</span></span>

## <span data-ttu-id="a02c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a02c7-102">SYNOPSIS</span></span>
<span data-ttu-id="a02c7-103">Anlık görüntü güncelleştirme nesnesinde görüntü başvurusu özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a02c7-103">Sets the image reference properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a02c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a02c7-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateImageReference [-SnapshotUpdate] <SnapshotUpdate> [[-Id] <String>] [[-Lun] <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a02c7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a02c7-105">DESCRIPTION</span></span>
<span data-ttu-id="a02c7-106">**Set-Azurermsnapshotupdateımagereference** cmdlet 'i, anlık görüntü güncelleştirme nesnesinde görüntü başvurusu özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a02c7-106">The **Set-AzureRmSnapshotUpdateImageReference** cmdlet sets the image reference properties on a snapshot update object.</span></span>

## <span data-ttu-id="a02c7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a02c7-107">EXAMPLES</span></span>

### <span data-ttu-id="a02c7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a02c7-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateImageReference -Snapshot $snapshotupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="a02c7-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel anlık görüntü güncelleştirme nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a02c7-109">The first command creates a local snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="a02c7-110">Ayrıca Windows işletim sistemi türünü de ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a02c7-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="a02c7-111">İkinci komut, anlık görüntü güncelleştirme nesnesi için resim kimliğini ve 0 mantıksal birim sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a02c7-111">The second command sets the image id and the logical unit number 0 for the snapshot update object.</span></span>
<span data-ttu-id="a02c7-112">Son komut, anlık görüntü güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adlı anlık görüntüyü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a02c7-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a02c7-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a02c7-113">PARAMETERS</span></span>

### <span data-ttu-id="a02c7-114">-ID</span><span class="sxs-lookup"><span data-stu-id="a02c7-114">-Id</span></span>
<span data-ttu-id="a02c7-115">KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a02c7-115">Specifies the ID.</span></span>

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

### <span data-ttu-id="a02c7-116">-LUN</span><span class="sxs-lookup"><span data-stu-id="a02c7-116">-Lun</span></span>
<span data-ttu-id="a02c7-117">Mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="a02c7-117">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="a02c7-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="a02c7-118">-SnapshotUpdate</span></span>
<span data-ttu-id="a02c7-119">Yerel anlık görüntü güncelleştirme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a02c7-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: SnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a02c7-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="a02c7-120">-Confirm</span></span>
<span data-ttu-id="a02c7-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a02c7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a02c7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a02c7-122">-WhatIf</span></span>
<span data-ttu-id="a02c7-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a02c7-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a02c7-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a02c7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a02c7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a02c7-125">CommonParameters</span></span>
<span data-ttu-id="a02c7-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a02c7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a02c7-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a02c7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a02c7-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a02c7-128">INPUTS</span></span>

### <span data-ttu-id="a02c7-129">Microsoft. Azure. Management. COMPUTE. modeller. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="a02c7-129">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="a02c7-130">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a02c7-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a02c7-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a02c7-131">OUTPUTS</span></span>

### <span data-ttu-id="a02c7-132">Microsoft. Azure. Management. COMPUTE. modeller. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="a02c7-132">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="a02c7-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a02c7-133">NOTES</span></span>

## <span data-ttu-id="a02c7-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a02c7-134">RELATED LINKS</span></span>

