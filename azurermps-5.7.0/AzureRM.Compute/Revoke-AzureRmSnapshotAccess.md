---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
ms.openlocfilehash: d081218a17bd5cac99256918d40ece722b73a85b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764468"
---
# <span data-ttu-id="2f232-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="2f232-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="2f232-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f232-102">SYNOPSIS</span></span>
<span data-ttu-id="2f232-103">Anlık görüntüye erişimi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="2f232-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f232-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f232-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f232-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f232-105">DESCRIPTION</span></span>
<span data-ttu-id="2f232-106">**Revoke-AzureRmSnapshotAccess** cmdlet 'i anlık görüntüye erişimi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="2f232-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="2f232-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f232-107">EXAMPLES</span></span>

### <span data-ttu-id="2f232-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2f232-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="2f232-109">' ResourceGroup01 ' adlı kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüye erişimi iptal etme</span><span class="sxs-lookup"><span data-stu-id="2f232-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="2f232-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f232-110">PARAMETERS</span></span>

### <span data-ttu-id="2f232-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f232-111">-ResourceGroupName</span></span>
<span data-ttu-id="2f232-112">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f232-112">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2f232-113">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="2f232-113">-SnapshotName</span></span>
<span data-ttu-id="2f232-114">Anlık görüntünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f232-114">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="2f232-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="2f232-115">-Confirm</span></span>
<span data-ttu-id="2f232-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2f232-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f232-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f232-117">-WhatIf</span></span>
<span data-ttu-id="2f232-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2f232-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f232-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2f232-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f232-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f232-120">CommonParameters</span></span>
<span data-ttu-id="2f232-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f232-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f232-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f232-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f232-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f232-123">INPUTS</span></span>

### <span data-ttu-id="2f232-124">System. String</span><span class="sxs-lookup"><span data-stu-id="2f232-124">System.String</span></span>

## <span data-ttu-id="2f232-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f232-125">OUTPUTS</span></span>

### <span data-ttu-id="2f232-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="2f232-126">System.Object</span></span>

## <span data-ttu-id="2f232-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f232-127">NOTES</span></span>

## <span data-ttu-id="2f232-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f232-128">RELATED LINKS</span></span>

