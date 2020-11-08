---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: 35e767c340d5418ae500c4cc87a4b40741d8ba6a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097570"
---
# <span data-ttu-id="3c58c-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="3c58c-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="3c58c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c58c-102">SYNOPSIS</span></span>
<span data-ttu-id="3c58c-103">Anlık görüntüye erişimi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="3c58c-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="3c58c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c58c-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c58c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c58c-105">DESCRIPTION</span></span>
<span data-ttu-id="3c58c-106">**Revoke-AzSnapshotAccess** cmdlet 'i anlık görüntüye erişimi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="3c58c-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="3c58c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c58c-107">EXAMPLES</span></span>

### <span data-ttu-id="3c58c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3c58c-108">Example 1</span></span>
```
PS C:\> Revoke-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="3c58c-109">' ResourceGroup01 ' adlı kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüye erişimi iptal etme</span><span class="sxs-lookup"><span data-stu-id="3c58c-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="3c58c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c58c-110">PARAMETERS</span></span>

### <span data-ttu-id="3c58c-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="3c58c-111">-AsJob</span></span>
<span data-ttu-id="3c58c-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3c58c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c58c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c58c-113">-DefaultProfile</span></span>
<span data-ttu-id="3c58c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3c58c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c58c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c58c-115">-ResourceGroupName</span></span>
<span data-ttu-id="3c58c-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c58c-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3c58c-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="3c58c-117">-SnapshotName</span></span>
<span data-ttu-id="3c58c-118">Anlık görüntünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c58c-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="3c58c-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="3c58c-119">-Confirm</span></span>
<span data-ttu-id="3c58c-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3c58c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c58c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c58c-121">-WhatIf</span></span>
<span data-ttu-id="3c58c-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c58c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c58c-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3c58c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c58c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c58c-124">CommonParameters</span></span>
<span data-ttu-id="3c58c-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c58c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c58c-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3c58c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c58c-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c58c-127">INPUTS</span></span>

### <span data-ttu-id="3c58c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3c58c-128">System.String</span></span>

## <span data-ttu-id="3c58c-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c58c-129">OUTPUTS</span></span>

### <span data-ttu-id="3c58c-130">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="3c58c-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3c58c-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c58c-131">NOTES</span></span>

## <span data-ttu-id="3c58c-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c58c-132">RELATED LINKS</span></span>