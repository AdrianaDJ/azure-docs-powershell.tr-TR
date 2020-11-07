---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
ms.openlocfilehash: 4e9a427a6e78848858773a1c661b949f91f0ffff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752791"
---
# <span data-ttu-id="d5952-101">Remove-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="d5952-101">Remove-AzSnapshot</span></span>

## <span data-ttu-id="d5952-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5952-102">SYNOPSIS</span></span>
<span data-ttu-id="d5952-103">Anlık görüntüyü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d5952-103">Removes a snapshot.</span></span>

## <span data-ttu-id="d5952-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5952-104">SYNTAX</span></span>

```
Remove-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5952-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5952-105">DESCRIPTION</span></span>
<span data-ttu-id="d5952-106">**Remove-AzSnapshot** cmdlet 'ini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d5952-106">The **Remove-AzSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="d5952-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5952-107">EXAMPLES</span></span>

### <span data-ttu-id="d5952-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d5952-108">Example 1</span></span>
```
PS C:\> Remove-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="d5952-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüyü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d5952-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d5952-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5952-110">PARAMETERS</span></span>

### <span data-ttu-id="d5952-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="d5952-111">-AsJob</span></span>
<span data-ttu-id="d5952-112">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="d5952-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d5952-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5952-113">-DefaultProfile</span></span>
<span data-ttu-id="d5952-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d5952-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5952-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d5952-115">-Force</span></span>
<span data-ttu-id="d5952-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="d5952-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d5952-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5952-117">-ResourceGroupName</span></span>
<span data-ttu-id="d5952-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5952-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d5952-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="d5952-119">-SnapshotName</span></span>
<span data-ttu-id="d5952-120">Anlık görüntünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5952-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="d5952-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="d5952-121">-Confirm</span></span>
<span data-ttu-id="d5952-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d5952-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5952-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5952-123">-WhatIf</span></span>
<span data-ttu-id="d5952-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d5952-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5952-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d5952-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5952-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5952-126">CommonParameters</span></span>
<span data-ttu-id="d5952-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5952-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5952-128">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d5952-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5952-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5952-129">INPUTS</span></span>

### <span data-ttu-id="d5952-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d5952-130">System.String</span></span>

## <span data-ttu-id="d5952-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5952-131">OUTPUTS</span></span>

### <span data-ttu-id="d5952-132">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="d5952-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="d5952-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5952-133">NOTES</span></span>

## <span data-ttu-id="d5952-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5952-134">RELATED LINKS</span></span>