---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
ms.openlocfilehash: 55a3a45cf22dd6558a9728a254531a0e01627e20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591696"
---
# <span data-ttu-id="646c6-101">Set-AzureRmDiskUpdateImageReference</span><span class="sxs-lookup"><span data-stu-id="646c6-101">Set-AzureRmDiskUpdateImageReference</span></span>

## <span data-ttu-id="646c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="646c6-102">SYNOPSIS</span></span>
<span data-ttu-id="646c6-103">Disk güncelleştirme nesnesinde görüntü başvurusu özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="646c6-103">Sets the image reference properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="646c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="646c6-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateImageReference [-DiskUpdate] <DiskUpdate> [[-Id] <String>] [[-Lun] <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="646c6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="646c6-105">DESCRIPTION</span></span>
<span data-ttu-id="646c6-106">**Set-Azurermdiskupdateımagereference** cmdlet 'i, bir disk güncelleştirme nesnesinde görüntü başvurusu özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="646c6-106">The **Set-AzureRmDiskUpdateImageReference** cmdlet sets the image reference properties on a disk update object.</span></span>

## <span data-ttu-id="646c6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="646c6-107">EXAMPLES</span></span>

### <span data-ttu-id="646c6-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="646c6-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateImageReference -Disk $diskupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="646c6-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir disk güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="646c6-109">The first command creates a local disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="646c6-110">Ayrıca Windows işletim sistemi türünü de ayarlar.</span><span class="sxs-lookup"><span data-stu-id="646c6-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="646c6-111">İkinci komut, görüntü kimliğini ve disk güncelleştirme nesnesi için 0 mantıksal birim sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="646c6-111">The second command sets the image id and the logical unit number 0 for the disk update object.</span></span>
<span data-ttu-id="646c6-112">Son komut, disk güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında var olan bir diski güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="646c6-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="646c6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="646c6-113">PARAMETERS</span></span>

### <span data-ttu-id="646c6-114">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="646c6-114">-DiskUpdate</span></span>
<span data-ttu-id="646c6-115">Yerel bir disk güncelleştirme nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="646c6-115">Specifies a local disk update object.</span></span>

```yaml
Type: DiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="646c6-116">-ID</span><span class="sxs-lookup"><span data-stu-id="646c6-116">-Id</span></span>
<span data-ttu-id="646c6-117">KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="646c6-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="646c6-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="646c6-118">-Lun</span></span>
<span data-ttu-id="646c6-119">Mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="646c6-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="646c6-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="646c6-120">-Confirm</span></span>
<span data-ttu-id="646c6-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="646c6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="646c6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="646c6-122">-WhatIf</span></span>
<span data-ttu-id="646c6-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="646c6-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="646c6-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="646c6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="646c6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="646c6-125">CommonParameters</span></span>
<span data-ttu-id="646c6-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="646c6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="646c6-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="646c6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="646c6-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="646c6-128">INPUTS</span></span>

### <span data-ttu-id="646c6-129">Microsoft. Azure. Management. COMPUTE. modeller. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="646c6-129">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="646c6-130">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="646c6-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="646c6-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="646c6-131">OUTPUTS</span></span>

### <span data-ttu-id="646c6-132">Microsoft. Azure. Management. COMPUTE. modeller. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="646c6-132">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="646c6-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="646c6-133">NOTES</span></span>

## <span data-ttu-id="646c6-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="646c6-134">RELATED LINKS</span></span>

