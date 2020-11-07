---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermdiskimagereference
schema: 2.0.0
ms.openlocfilehash: cd0a66d8f8d777df9a8ebc3791643234f0d15fb0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939580"
---
# <span data-ttu-id="4dae5-101">Set-AzureRmDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="4dae5-101">Set-AzureRmDiskImageReference</span></span>

## <span data-ttu-id="4dae5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dae5-102">SYNOPSIS</span></span>
<span data-ttu-id="4dae5-103">Disk nesnesinde görüntü başvuru özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4dae5-103">Sets the image reference properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4dae5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4dae5-104">SYNTAX</span></span>

```
Set-AzureRmDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dae5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4dae5-105">DESCRIPTION</span></span>
<span data-ttu-id="4dae5-106">**Set-Azurermdiskımagereference** cmdlet 'i, bir disk nesnesindeki görüntü başvurusu özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4dae5-106">The **Set-AzureRmDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="4dae5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4dae5-107">EXAMPLES</span></span>

### <span data-ttu-id="4dae5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4dae5-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzureRmDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="4dae5-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4dae5-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="4dae5-110">Ayrıca Windows işletim sistemi türünü de ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4dae5-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="4dae5-111">İkinci komut, görüntü kimliğini ve disk nesnesi için 0 mantıksal birim sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4dae5-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="4dae5-112">Son komut, disk nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4dae5-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4dae5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4dae5-113">PARAMETERS</span></span>

### <span data-ttu-id="4dae5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dae5-114">-DefaultProfile</span></span>
<span data-ttu-id="4dae5-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4dae5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4dae5-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="4dae5-116">-Disk</span></span>
<span data-ttu-id="4dae5-117">Yerel bir disk nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4dae5-117">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4dae5-118">-ID</span><span class="sxs-lookup"><span data-stu-id="4dae5-118">-Id</span></span>
<span data-ttu-id="4dae5-119">KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4dae5-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="4dae5-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="4dae5-120">-Lun</span></span>
<span data-ttu-id="4dae5-121">Mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="4dae5-121">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="4dae5-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="4dae5-122">-Confirm</span></span>
<span data-ttu-id="4dae5-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4dae5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dae5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dae5-124">-WhatIf</span></span>
<span data-ttu-id="4dae5-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4dae5-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4dae5-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4dae5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dae5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dae5-127">CommonParameters</span></span>
<span data-ttu-id="4dae5-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4dae5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dae5-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dae5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dae5-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4dae5-130">INPUTS</span></span>

### <span data-ttu-id="4dae5-131">Microsoft. Azure. Management. COMPUTE. modeller. disk</span><span class="sxs-lookup"><span data-stu-id="4dae5-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="4dae5-132">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4dae5-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="4dae5-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4dae5-133">OUTPUTS</span></span>

### <span data-ttu-id="4dae5-134">Microsoft. Azure. Management. COMPUTE. modeller. disk</span><span class="sxs-lookup"><span data-stu-id="4dae5-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="4dae5-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4dae5-135">NOTES</span></span>

## <span data-ttu-id="4dae5-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4dae5-136">RELATED LINKS</span></span>

