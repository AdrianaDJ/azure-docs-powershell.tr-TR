---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 5c0af3ed67bd7cba3408b6628de70c7064120954
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276514"
---
# <span data-ttu-id="06a3d-101">New-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="06a3d-101">New-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="06a3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06a3d-102">SYNOPSIS</span></span>
<span data-ttu-id="06a3d-103">Aygıttaki Edge depolama hesabında yeni bir depolama kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06a3d-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="06a3d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06a3d-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06a3d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="06a3d-105">DESCRIPTION</span></span>
<span data-ttu-id="06a3d-106">**New-AzStackEdgeStorageContainer** cmdlet 'i, bir yığın uç cihazında Edge depolama hesabında yeni bir depolama kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06a3d-106">The **New-AzStackEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Stack Edge device.</span></span>

## <span data-ttu-id="06a3d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06a3d-107">EXAMPLES</span></span>

### <span data-ttu-id="06a3d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="06a3d-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="06a3d-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06a3d-109">PARAMETERS</span></span>

### <span data-ttu-id="06a3d-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="06a3d-110">-AsJob</span></span>
<span data-ttu-id="06a3d-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="06a3d-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06a3d-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="06a3d-112">-DataFormat</span></span>
<span data-ttu-id="06a3d-113">Veri biçimini ayarla Ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="06a3d-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="06a3d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06a3d-114">-DefaultProfile</span></span>
<span data-ttu-id="06a3d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="06a3d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06a3d-116">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="06a3d-116">-DeviceName</span></span>
<span data-ttu-id="06a3d-117">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="06a3d-117">Device Name</span></span>

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

### <span data-ttu-id="06a3d-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="06a3d-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="06a3d-119">Var olan EdgeStorageAccount adının adını sağlayın</span><span class="sxs-lookup"><span data-stu-id="06a3d-119">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="06a3d-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="06a3d-120">-Name</span></span>
<span data-ttu-id="06a3d-121">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="06a3d-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06a3d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06a3d-122">-ResourceGroupName</span></span>
<span data-ttu-id="06a3d-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="06a3d-123">Resource Group Name</span></span>

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

### <span data-ttu-id="06a3d-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="06a3d-124">-Confirm</span></span>
<span data-ttu-id="06a3d-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="06a3d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06a3d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06a3d-126">-WhatIf</span></span>
<span data-ttu-id="06a3d-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="06a3d-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06a3d-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="06a3d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06a3d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06a3d-129">CommonParameters</span></span>
<span data-ttu-id="06a3d-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06a3d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06a3d-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="06a3d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06a3d-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06a3d-132">INPUTS</span></span>

### <span data-ttu-id="06a3d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="06a3d-133">System.String</span></span>

## <span data-ttu-id="06a3d-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06a3d-134">OUTPUTS</span></span>

### <span data-ttu-id="06a3d-135">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="06a3d-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="06a3d-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06a3d-136">NOTES</span></span>

## <span data-ttu-id="06a3d-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06a3d-137">RELATED LINKS</span></span>
