---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: 36dec1f8d4374f2e5bbed1f742aa7733bb760f67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589863"
---
# <span data-ttu-id="f2dfd-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="f2dfd-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="f2dfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="f2dfd-103">Anlık görüntüyü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f2dfd-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2dfd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2dfd-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2dfd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2dfd-105">DESCRIPTION</span></span>
<span data-ttu-id="f2dfd-106">**Remove-AzureRmSnapshot** cmdlet 'ini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f2dfd-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="f2dfd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2dfd-107">EXAMPLES</span></span>

### <span data-ttu-id="f2dfd-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f2dfd-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="f2dfd-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüyü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f2dfd-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f2dfd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2dfd-110">PARAMETERS</span></span>

### <span data-ttu-id="f2dfd-111">-Force</span><span class="sxs-lookup"><span data-stu-id="f2dfd-111">-Force</span></span>
<span data-ttu-id="f2dfd-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f2dfd-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2dfd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2dfd-113">-ResourceGroupName</span></span>
<span data-ttu-id="f2dfd-114">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2dfd-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f2dfd-115">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="f2dfd-115">-SnapshotName</span></span>
<span data-ttu-id="f2dfd-116">Anlık görüntünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2dfd-116">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="f2dfd-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="f2dfd-117">-Confirm</span></span>
<span data-ttu-id="f2dfd-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f2dfd-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2dfd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2dfd-119">-WhatIf</span></span>
<span data-ttu-id="f2dfd-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f2dfd-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2dfd-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f2dfd-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2dfd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2dfd-122">CommonParameters</span></span>
<span data-ttu-id="f2dfd-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2dfd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2dfd-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2dfd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2dfd-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2dfd-125">INPUTS</span></span>

### <span data-ttu-id="f2dfd-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f2dfd-126">System.String</span></span>

## <span data-ttu-id="f2dfd-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2dfd-127">OUTPUTS</span></span>

### <span data-ttu-id="f2dfd-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="f2dfd-128">System.Object</span></span>

## <span data-ttu-id="f2dfd-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2dfd-129">NOTES</span></span>

## <span data-ttu-id="f2dfd-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2dfd-130">RELATED LINKS</span></span>

