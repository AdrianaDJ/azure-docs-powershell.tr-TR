---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
ms.openlocfilehash: bbaa82500e06f426dd5b7496849507b91a599da6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762274"
---
# <span data-ttu-id="09925-101">Set-AzureRmSnapshotUpdateImageReference</span><span class="sxs-lookup"><span data-stu-id="09925-101">Set-AzureRmSnapshotUpdateImageReference</span></span>

## <span data-ttu-id="09925-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09925-102">SYNOPSIS</span></span>
<span data-ttu-id="09925-103">Anlık görüntü güncelleştirme nesnesinde görüntü başvurusu özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="09925-103">Sets the image reference properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09925-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="09925-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateImageReference [-SnapshotUpdate] <PSSnapshotUpdate> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09925-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="09925-105">DESCRIPTION</span></span>
<span data-ttu-id="09925-106">**Set-Azurermsnapshotupdateımagereference** cmdlet 'i, anlık görüntü güncelleştirme nesnesinde görüntü başvurusu özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="09925-106">The **Set-AzureRmSnapshotUpdateImageReference** cmdlet sets the image reference properties on a snapshot update object.</span></span>

## <span data-ttu-id="09925-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="09925-107">EXAMPLES</span></span>

### <span data-ttu-id="09925-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="09925-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateImageReference -Snapshot $snapshotupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="09925-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel anlık görüntü güncelleştirme nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="09925-109">The first command creates a local snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="09925-110">Ayrıca Windows işletim sistemi türünü de ayarlar.</span><span class="sxs-lookup"><span data-stu-id="09925-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="09925-111">İkinci komut, anlık görüntü güncelleştirme nesnesi için resim kimliğini ve 0 mantıksal birim sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="09925-111">The second command sets the image id and the logical unit number 0 for the snapshot update object.</span></span>
<span data-ttu-id="09925-112">Son komut, anlık görüntü güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adlı anlık görüntüyü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="09925-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="09925-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="09925-113">PARAMETERS</span></span>

### <span data-ttu-id="09925-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09925-114">-DefaultProfile</span></span>
<span data-ttu-id="09925-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="09925-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09925-116">-ID</span><span class="sxs-lookup"><span data-stu-id="09925-116">-Id</span></span>
<span data-ttu-id="09925-117">KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="09925-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="09925-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="09925-118">-Lun</span></span>
<span data-ttu-id="09925-119">Mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="09925-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="09925-120">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="09925-120">-SnapshotUpdate</span></span>
<span data-ttu-id="09925-121">Yerel anlık görüntü güncelleştirme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="09925-121">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09925-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="09925-122">-Confirm</span></span>
<span data-ttu-id="09925-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="09925-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09925-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09925-124">-WhatIf</span></span>
<span data-ttu-id="09925-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="09925-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09925-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="09925-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09925-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09925-127">CommonParameters</span></span>
<span data-ttu-id="09925-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="09925-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09925-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09925-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09925-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="09925-130">INPUTS</span></span>

### <span data-ttu-id="09925-131">Microsoft. Azure. Management. COMPUTE. modeller. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="09925-131">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="09925-132">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="09925-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="09925-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="09925-133">OUTPUTS</span></span>

### <span data-ttu-id="09925-134">Microsoft. Azure. Management. COMPUTE. modeller. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="09925-134">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="09925-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="09925-135">NOTES</span></span>

## <span data-ttu-id="09925-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="09925-136">RELATED LINKS</span></span>

