---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 3561c77e79f0ee1be82b8f180fdf1b73879dc084
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268025"
---
# <span data-ttu-id="00581-101">New-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="00581-101">New-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="00581-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00581-102">SYNOPSIS</span></span>
<span data-ttu-id="00581-103">Aygıttaki Edge depolama hesabında yeni bir depolama kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="00581-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="00581-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00581-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00581-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="00581-105">DESCRIPTION</span></span>
<span data-ttu-id="00581-106">**New-AzDataBoxEdgeStorageContainer** cmdlet 'i, bir veri kutusu uç aygıtındaki uç depolama hesabında yeni bir depolama kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="00581-106">The **New-AzDataBoxEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Data Box Edge device.</span></span>

## <span data-ttu-id="00581-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00581-107">EXAMPLES</span></span>

### <span data-ttu-id="00581-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="00581-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="00581-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00581-109">PARAMETERS</span></span>

### <span data-ttu-id="00581-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="00581-110">-AsJob</span></span>
<span data-ttu-id="00581-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="00581-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00581-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="00581-112">-DataFormat</span></span>
<span data-ttu-id="00581-113">Veri biçimini ayarla Ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="00581-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00581-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00581-114">-DefaultProfile</span></span>
<span data-ttu-id="00581-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="00581-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00581-116">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="00581-116">-DeviceName</span></span>
<span data-ttu-id="00581-117">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="00581-117">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00581-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="00581-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="00581-119">Var olan EdgeStorageAccount adının adını sağlayın</span><span class="sxs-lookup"><span data-stu-id="00581-119">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00581-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="00581-120">-Name</span></span>
<span data-ttu-id="00581-121">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="00581-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00581-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00581-122">-ResourceGroupName</span></span>
<span data-ttu-id="00581-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="00581-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00581-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="00581-124">-Confirm</span></span>
<span data-ttu-id="00581-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="00581-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00581-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00581-126">-WhatIf</span></span>
<span data-ttu-id="00581-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="00581-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00581-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="00581-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00581-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00581-129">CommonParameters</span></span>
<span data-ttu-id="00581-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00581-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00581-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="00581-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00581-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00581-132">INPUTS</span></span>

### <span data-ttu-id="00581-133">System. String</span><span class="sxs-lookup"><span data-stu-id="00581-133">System.String</span></span>

## <span data-ttu-id="00581-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00581-134">OUTPUTS</span></span>

### <span data-ttu-id="00581-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="00581-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="00581-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00581-136">NOTES</span></span>

## <span data-ttu-id="00581-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00581-137">RELATED LINKS</span></span>
