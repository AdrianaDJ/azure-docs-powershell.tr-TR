---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
ms.openlocfilehash: 10150d7941aa3b17a0a7d4447ff0a57e3d04a516
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587609"
---
# <span data-ttu-id="6bae1-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="6bae1-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="6bae1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bae1-102">SYNOPSIS</span></span>
<span data-ttu-id="6bae1-103">Diski kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6bae1-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bae1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6bae1-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6bae1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6bae1-105">DESCRIPTION</span></span>
<span data-ttu-id="6bae1-106">**Remove-Azurermdısk** cmdlet 'i diski kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6bae1-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="6bae1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6bae1-107">EXAMPLES</span></span>

### <span data-ttu-id="6bae1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6bae1-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="6bae1-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Disk01 ' adlı diski kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6bae1-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6bae1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6bae1-110">PARAMETERS</span></span>

### <span data-ttu-id="6bae1-111">-DiskName</span><span class="sxs-lookup"><span data-stu-id="6bae1-111">-DiskName</span></span>
<span data-ttu-id="6bae1-112">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bae1-112">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="6bae1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6bae1-113">-Force</span></span>
<span data-ttu-id="6bae1-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="6bae1-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6bae1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bae1-115">-ResourceGroupName</span></span>
<span data-ttu-id="6bae1-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bae1-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6bae1-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="6bae1-117">-Confirm</span></span>
<span data-ttu-id="6bae1-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6bae1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bae1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bae1-119">-WhatIf</span></span>
<span data-ttu-id="6bae1-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6bae1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bae1-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6bae1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bae1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bae1-122">CommonParameters</span></span>
<span data-ttu-id="6bae1-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6bae1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bae1-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bae1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bae1-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6bae1-125">INPUTS</span></span>

### <span data-ttu-id="6bae1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6bae1-126">System.String</span></span>

## <span data-ttu-id="6bae1-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6bae1-127">OUTPUTS</span></span>

### <span data-ttu-id="6bae1-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="6bae1-128">System.Object</span></span>

## <span data-ttu-id="6bae1-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6bae1-129">NOTES</span></span>

## <span data-ttu-id="6bae1-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6bae1-130">RELATED LINKS</span></span>

