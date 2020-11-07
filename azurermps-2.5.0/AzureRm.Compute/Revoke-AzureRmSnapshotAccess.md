---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermsnapshotaccess
schema: 2.0.0
ms.openlocfilehash: bbde391c56d4b50320f15441b75b93d125771ccb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940179"
---
# <span data-ttu-id="860e7-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="860e7-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="860e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="860e7-102">SYNOPSIS</span></span>
<span data-ttu-id="860e7-103">Anlık görüntüye erişimi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="860e7-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="860e7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="860e7-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="860e7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="860e7-105">DESCRIPTION</span></span>
<span data-ttu-id="860e7-106">**Revoke-AzureRmSnapshotAccess** cmdlet 'i anlık görüntüye erişimi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="860e7-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="860e7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="860e7-107">EXAMPLES</span></span>

### <span data-ttu-id="860e7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="860e7-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="860e7-109">' ResourceGroup01 ' adlı kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüye erişimi iptal etme</span><span class="sxs-lookup"><span data-stu-id="860e7-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="860e7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="860e7-110">PARAMETERS</span></span>

### <span data-ttu-id="860e7-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="860e7-111">-AsJob</span></span>
<span data-ttu-id="860e7-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="860e7-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="860e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="860e7-113">-DefaultProfile</span></span>
<span data-ttu-id="860e7-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="860e7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="860e7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="860e7-115">-ResourceGroupName</span></span>
<span data-ttu-id="860e7-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="860e7-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="860e7-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="860e7-117">-SnapshotName</span></span>
<span data-ttu-id="860e7-118">Anlık görüntünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="860e7-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="860e7-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="860e7-119">-Confirm</span></span>
<span data-ttu-id="860e7-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="860e7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="860e7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="860e7-121">-WhatIf</span></span>
<span data-ttu-id="860e7-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="860e7-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="860e7-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="860e7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="860e7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="860e7-124">CommonParameters</span></span>
<span data-ttu-id="860e7-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="860e7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="860e7-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="860e7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="860e7-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="860e7-127">INPUTS</span></span>

### <span data-ttu-id="860e7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="860e7-128">System.String</span></span>

## <span data-ttu-id="860e7-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="860e7-129">OUTPUTS</span></span>

### <span data-ttu-id="860e7-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="860e7-130">System.Object</span></span>

## <span data-ttu-id="860e7-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="860e7-131">NOTES</span></span>

## <span data-ttu-id="860e7-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="860e7-132">RELATED LINKS</span></span>

