---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: deb122735b94ed8ac0de63330a9fbdb3ecac81d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277497"
---
# <span data-ttu-id="55ed2-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="55ed2-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="55ed2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="55ed2-103">Anlık görüntü nesnesinde görüntü başvurusu özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="55ed2-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="55ed2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55ed2-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55ed2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="55ed2-105">DESCRIPTION</span></span>
<span data-ttu-id="55ed2-106">**Set-azgörüntütıgereference** cmdlet 'i, anlık görüntü nesnesinde görüntü başvurusu özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="55ed2-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="55ed2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55ed2-107">EXAMPLES</span></span>

### <span data-ttu-id="55ed2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="55ed2-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="55ed2-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 GB olan yerel bir anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="55ed2-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="55ed2-110">Ayrıca Windows işletim sistemi türünü de ayarlar.</span><span class="sxs-lookup"><span data-stu-id="55ed2-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="55ed2-111">İkinci komut, anlık görüntü nesnesinin görüntü KIMLIĞINI ve 0 mantıksal birim sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="55ed2-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="55ed2-112">Son komut, Snapshot nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adıyla bir anlık görüntü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="55ed2-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="55ed2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55ed2-113">PARAMETERS</span></span>

### <span data-ttu-id="55ed2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55ed2-114">-DefaultProfile</span></span>
<span data-ttu-id="55ed2-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55ed2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ed2-116">-ID</span><span class="sxs-lookup"><span data-stu-id="55ed2-116">-Id</span></span>
<span data-ttu-id="55ed2-117">KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="55ed2-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="55ed2-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="55ed2-118">-Lun</span></span>
<span data-ttu-id="55ed2-119">Mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="55ed2-119">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55ed2-120">-Anlık görüntü</span><span class="sxs-lookup"><span data-stu-id="55ed2-120">-Snapshot</span></span>
<span data-ttu-id="55ed2-121">Yerel bir anlık görüntü nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="55ed2-121">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55ed2-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="55ed2-122">-Confirm</span></span>
<span data-ttu-id="55ed2-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="55ed2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55ed2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55ed2-124">-WhatIf</span></span>
<span data-ttu-id="55ed2-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="55ed2-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55ed2-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="55ed2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55ed2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55ed2-127">CommonParameters</span></span>
<span data-ttu-id="55ed2-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55ed2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55ed2-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="55ed2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55ed2-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55ed2-130">INPUTS</span></span>

### <span data-ttu-id="55ed2-131">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="55ed2-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="55ed2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="55ed2-132">System.String</span></span>

### <span data-ttu-id="55ed2-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="55ed2-133">System.Int32</span></span>

## <span data-ttu-id="55ed2-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55ed2-134">OUTPUTS</span></span>

### <span data-ttu-id="55ed2-135">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="55ed2-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="55ed2-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55ed2-136">NOTES</span></span>

## <span data-ttu-id="55ed2-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55ed2-137">RELATED LINKS</span></span>
