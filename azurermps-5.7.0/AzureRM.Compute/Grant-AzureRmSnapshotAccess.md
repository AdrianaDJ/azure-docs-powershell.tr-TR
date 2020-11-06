---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
ms.openlocfilehash: 8f68957020d8e4607477bd78cc42b05c29e321c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586804"
---
# <span data-ttu-id="107c0-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="107c0-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="107c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="107c0-102">SYNOPSIS</span></span>
<span data-ttu-id="107c0-103">Anlık görüntüye erişim verir.</span><span class="sxs-lookup"><span data-stu-id="107c0-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="107c0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="107c0-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="107c0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="107c0-105">DESCRIPTION</span></span>
<span data-ttu-id="107c0-106">**Grant-AzureRmSnapshotAccess** cmdlet 'i anlık görüntüye erişim verir.</span><span class="sxs-lookup"><span data-stu-id="107c0-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="107c0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="107c0-107">EXAMPLES</span></span>

### <span data-ttu-id="107c0-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="107c0-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="107c0-109">60 saniye için ' ResourceGroup01 ' adındaki kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüye ' Read ' erişimi verin.</span><span class="sxs-lookup"><span data-stu-id="107c0-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="107c0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="107c0-110">PARAMETERS</span></span>

### <span data-ttu-id="107c0-111">-Access</span><span class="sxs-lookup"><span data-stu-id="107c0-111">-Access</span></span>
<span data-ttu-id="107c0-112">Erişim düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="107c0-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="107c0-113">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="107c0-113">-DurationInSecond</span></span>
<span data-ttu-id="107c0-114">Erişim süresini saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="107c0-114">Specifies access duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="107c0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="107c0-115">-ResourceGroupName</span></span>
<span data-ttu-id="107c0-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="107c0-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="107c0-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="107c0-117">-SnapshotName</span></span>
<span data-ttu-id="107c0-118">Anlık görüntünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="107c0-118">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="107c0-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="107c0-119">-Confirm</span></span>
<span data-ttu-id="107c0-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="107c0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="107c0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="107c0-121">-WhatIf</span></span>
<span data-ttu-id="107c0-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="107c0-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="107c0-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="107c0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="107c0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="107c0-124">CommonParameters</span></span>
<span data-ttu-id="107c0-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="107c0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="107c0-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="107c0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="107c0-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="107c0-127">INPUTS</span></span>

### <span data-ttu-id="107c0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="107c0-128">System.String</span></span>

## <span data-ttu-id="107c0-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="107c0-129">OUTPUTS</span></span>

### <span data-ttu-id="107c0-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="107c0-130">System.Object</span></span>

## <span data-ttu-id="107c0-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="107c0-131">NOTES</span></span>

## <span data-ttu-id="107c0-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="107c0-132">RELATED LINKS</span></span>

