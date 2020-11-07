---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: 18d459603923c64c0b38e5d092faf1928c73bb3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752881"
---
# <span data-ttu-id="9ef00-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="9ef00-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="9ef00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ef00-102">SYNOPSIS</span></span>
<span data-ttu-id="9ef00-103">Anlık görüntüye erişim verir.</span><span class="sxs-lookup"><span data-stu-id="9ef00-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="9ef00-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ef00-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ef00-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ef00-105">DESCRIPTION</span></span>
<span data-ttu-id="9ef00-106">**Grant-AzSnapshotAccess** cmdlet 'i anlık görüntüye erişim verir.</span><span class="sxs-lookup"><span data-stu-id="9ef00-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="9ef00-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ef00-107">EXAMPLES</span></span>

### <span data-ttu-id="9ef00-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9ef00-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="9ef00-109">60 saniye için ' ResourceGroup01 ' adındaki kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüye ' Read ' erişimi verin.</span><span class="sxs-lookup"><span data-stu-id="9ef00-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="9ef00-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ef00-110">PARAMETERS</span></span>

### <span data-ttu-id="9ef00-111">-Access</span><span class="sxs-lookup"><span data-stu-id="9ef00-111">-Access</span></span>
<span data-ttu-id="9ef00-112">Erişim düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ef00-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef00-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="9ef00-113">-AsJob</span></span>
<span data-ttu-id="9ef00-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9ef00-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ef00-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ef00-115">-DefaultProfile</span></span>
<span data-ttu-id="9ef00-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9ef00-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ef00-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="9ef00-117">-DurationInSecond</span></span>
<span data-ttu-id="9ef00-118">Erişim süresini saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ef00-118">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef00-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ef00-119">-ResourceGroupName</span></span>
<span data-ttu-id="9ef00-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ef00-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9ef00-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="9ef00-121">-SnapshotName</span></span>
<span data-ttu-id="9ef00-122">Anlık görüntünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ef00-122">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ef00-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="9ef00-123">-Confirm</span></span>
<span data-ttu-id="9ef00-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9ef00-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ef00-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ef00-125">-WhatIf</span></span>
<span data-ttu-id="9ef00-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9ef00-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ef00-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9ef00-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ef00-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ef00-128">CommonParameters</span></span>
<span data-ttu-id="9ef00-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ef00-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ef00-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9ef00-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ef00-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ef00-131">INPUTS</span></span>

### <span data-ttu-id="9ef00-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9ef00-132">System.String</span></span>

## <span data-ttu-id="9ef00-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ef00-133">OUTPUTS</span></span>

### <span data-ttu-id="9ef00-134">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="9ef00-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="9ef00-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ef00-135">NOTES</span></span>

## <span data-ttu-id="9ef00-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ef00-136">RELATED LINKS</span></span>