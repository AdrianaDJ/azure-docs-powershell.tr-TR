---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermsnapshotimagereference
schema: 2.0.0
ms.openlocfilehash: d3ad489ae1e61b1e2543f7ef75fae2fd93e33a03
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938976"
---
# <span data-ttu-id="8db4d-101">Set-AzureRmSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="8db4d-101">Set-AzureRmSnapshotImageReference</span></span>

## <span data-ttu-id="8db4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8db4d-102">SYNOPSIS</span></span>
<span data-ttu-id="8db4d-103">Anlık görüntü nesnesinde görüntü başvurusu özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8db4d-103">Sets the image reference properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8db4d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8db4d-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8db4d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8db4d-105">DESCRIPTION</span></span>
<span data-ttu-id="8db4d-106">**Set-Azurermsnapshotıgereference** cmdlet 'i, anlık görüntü nesnesinde görüntü başvurusu özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8db4d-106">The **Set-AzureRmSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="8db4d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8db4d-107">EXAMPLES</span></span>

### <span data-ttu-id="8db4d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8db4d-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzureRmSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="8db4d-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 GB olan yerel bir anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8db4d-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="8db4d-110">Ayrıca Windows işletim sistemi türünü de ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8db4d-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="8db4d-111">İkinci komut, anlık görüntü nesnesinin görüntü KIMLIĞINI ve 0 mantıksal birim sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8db4d-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="8db4d-112">Son komut, Snapshot nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adıyla bir anlık görüntü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8db4d-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="8db4d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8db4d-113">PARAMETERS</span></span>

### <span data-ttu-id="8db4d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8db4d-114">-DefaultProfile</span></span>
<span data-ttu-id="8db4d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8db4d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8db4d-116">-ID</span><span class="sxs-lookup"><span data-stu-id="8db4d-116">-Id</span></span>
<span data-ttu-id="8db4d-117">KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8db4d-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="8db4d-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="8db4d-118">-Lun</span></span>
<span data-ttu-id="8db4d-119">Mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="8db4d-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="8db4d-120">-Anlık görüntü</span><span class="sxs-lookup"><span data-stu-id="8db4d-120">-Snapshot</span></span>
<span data-ttu-id="8db4d-121">Yerel bir anlık görüntü nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8db4d-121">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8db4d-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="8db4d-122">-Confirm</span></span>
<span data-ttu-id="8db4d-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8db4d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8db4d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8db4d-124">-WhatIf</span></span>
<span data-ttu-id="8db4d-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8db4d-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8db4d-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8db4d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8db4d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8db4d-127">CommonParameters</span></span>
<span data-ttu-id="8db4d-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8db4d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8db4d-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8db4d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8db4d-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8db4d-130">INPUTS</span></span>

### <span data-ttu-id="8db4d-131">Microsoft. Azure. Management. COMPUTE. modeller. anlık görüntüsü</span><span class="sxs-lookup"><span data-stu-id="8db4d-131">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="8db4d-132">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8db4d-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="8db4d-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8db4d-133">OUTPUTS</span></span>

### <span data-ttu-id="8db4d-134">Microsoft. Azure. Management. COMPUTE. modeller. anlık görüntüsü</span><span class="sxs-lookup"><span data-stu-id="8db4d-134">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="8db4d-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8db4d-135">NOTES</span></span>

## <span data-ttu-id="8db4d-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8db4d-136">RELATED LINKS</span></span>

