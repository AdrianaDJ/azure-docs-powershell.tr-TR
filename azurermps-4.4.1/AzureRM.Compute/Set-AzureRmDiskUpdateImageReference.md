---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
ms.openlocfilehash: 777216f6969e661721785601a21ee9604d5eec94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764895"
---
# <span data-ttu-id="36b3f-101">Set-AzureRmDiskUpdateImageReference</span><span class="sxs-lookup"><span data-stu-id="36b3f-101">Set-AzureRmDiskUpdateImageReference</span></span>

## <span data-ttu-id="36b3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="36b3f-103">Disk güncelleştirme nesnesinde görüntü başvurusu özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="36b3f-103">Sets the image reference properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36b3f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36b3f-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateImageReference [-DiskUpdate] <PSDiskUpdate> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36b3f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="36b3f-105">DESCRIPTION</span></span>
<span data-ttu-id="36b3f-106">**Set-Azurermdiskupdateımagereference** cmdlet 'i, bir disk güncelleştirme nesnesinde görüntü başvurusu özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="36b3f-106">The **Set-AzureRmDiskUpdateImageReference** cmdlet sets the image reference properties on a disk update object.</span></span>

## <span data-ttu-id="36b3f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36b3f-107">EXAMPLES</span></span>

### <span data-ttu-id="36b3f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="36b3f-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateImageReference -Disk $diskupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="36b3f-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir disk güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="36b3f-109">The first command creates a local disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="36b3f-110">Ayrıca Windows işletim sistemi türünü de ayarlar.</span><span class="sxs-lookup"><span data-stu-id="36b3f-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="36b3f-111">İkinci komut, görüntü kimliğini ve disk güncelleştirme nesnesi için 0 mantıksal birim sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="36b3f-111">The second command sets the image id and the logical unit number 0 for the disk update object.</span></span>
<span data-ttu-id="36b3f-112">Son komut, disk güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında var olan bir diski güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="36b3f-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="36b3f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36b3f-113">PARAMETERS</span></span>

### <span data-ttu-id="36b3f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b3f-114">-DefaultProfile</span></span>
<span data-ttu-id="36b3f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="36b3f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36b3f-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="36b3f-116">-DiskUpdate</span></span>
<span data-ttu-id="36b3f-117">Yerel bir disk güncelleştirme nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="36b3f-117">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36b3f-118">-ID</span><span class="sxs-lookup"><span data-stu-id="36b3f-118">-Id</span></span>
<span data-ttu-id="36b3f-119">KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="36b3f-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="36b3f-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="36b3f-120">-Lun</span></span>
<span data-ttu-id="36b3f-121">Mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="36b3f-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b3f-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="36b3f-122">-Confirm</span></span>
<span data-ttu-id="36b3f-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="36b3f-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b3f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36b3f-124">-WhatIf</span></span>
<span data-ttu-id="36b3f-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="36b3f-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36b3f-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="36b3f-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b3f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b3f-127">CommonParameters</span></span>
<span data-ttu-id="36b3f-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36b3f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b3f-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36b3f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b3f-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36b3f-130">INPUTS</span></span>

### <span data-ttu-id="36b3f-131">Microsoft. Azure. Management. COMPUTE. modeller. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="36b3f-131">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="36b3f-132">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="36b3f-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="36b3f-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36b3f-133">OUTPUTS</span></span>

### <span data-ttu-id="36b3f-134">Microsoft. Azure. Management. COMPUTE. modeller. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="36b3f-134">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="36b3f-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36b3f-135">NOTES</span></span>

## <span data-ttu-id="36b3f-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36b3f-136">RELATED LINKS</span></span>

