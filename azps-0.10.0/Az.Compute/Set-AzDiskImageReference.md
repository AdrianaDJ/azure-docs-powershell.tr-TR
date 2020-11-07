---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskImageReference.md
ms.openlocfilehash: 25bf6699887219cb4315465d7e0f709f82849438
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936871"
---
# <span data-ttu-id="3bd05-101">Set-AzDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="3bd05-101">Set-AzDiskImageReference</span></span>

## <span data-ttu-id="3bd05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bd05-102">SYNOPSIS</span></span>
<span data-ttu-id="3bd05-103">Disk nesnesinde görüntü başvuru özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3bd05-103">Sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="3bd05-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3bd05-104">SYNTAX</span></span>

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bd05-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3bd05-105">DESCRIPTION</span></span>
<span data-ttu-id="3bd05-106">**Set-Azdiskımagereference** cmdlet 'i, bir disk nesnesindeki görüntü başvurusu özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3bd05-106">The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="3bd05-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3bd05-107">EXAMPLES</span></span>

### <span data-ttu-id="3bd05-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3bd05-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="3bd05-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3bd05-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="3bd05-110">Ayrıca Windows işletim sistemi türünü de ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3bd05-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="3bd05-111">İkinci komut, disk için görüntü kimliğini ve 0 mantıksal birim sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3bd05-111">The second command sets the image id and the logical unit number 0 for the disk obejct.</span></span>
<span data-ttu-id="3bd05-112">Son komut, disk nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3bd05-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3bd05-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3bd05-113">PARAMETERS</span></span>

### <span data-ttu-id="3bd05-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bd05-114">-DefaultProfile</span></span>
<span data-ttu-id="3bd05-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3bd05-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bd05-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="3bd05-116">-Disk</span></span>
<span data-ttu-id="3bd05-117">Yerel bir disk nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3bd05-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="3bd05-118">-ID</span><span class="sxs-lookup"><span data-stu-id="3bd05-118">-Id</span></span>
<span data-ttu-id="3bd05-119">KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3bd05-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="3bd05-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="3bd05-120">-Lun</span></span>
<span data-ttu-id="3bd05-121">Mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="3bd05-121">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="3bd05-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="3bd05-122">-Confirm</span></span>
<span data-ttu-id="3bd05-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3bd05-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bd05-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bd05-124">-WhatIf</span></span>
<span data-ttu-id="3bd05-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3bd05-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3bd05-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3bd05-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bd05-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd05-127">CommonParameters</span></span>
<span data-ttu-id="3bd05-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3bd05-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd05-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bd05-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd05-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3bd05-130">INPUTS</span></span>

### <span data-ttu-id="3bd05-131">Microsoft. Azure. Management. COMPUTE. modeller. disk</span><span class="sxs-lookup"><span data-stu-id="3bd05-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="3bd05-132">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="3bd05-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="3bd05-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3bd05-133">OUTPUTS</span></span>

### <span data-ttu-id="3bd05-134">Microsoft. Azure. Management. COMPUTE. modeller. disk</span><span class="sxs-lookup"><span data-stu-id="3bd05-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="3bd05-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3bd05-135">NOTES</span></span>

## <span data-ttu-id="3bd05-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3bd05-136">RELATED LINKS</span></span>

